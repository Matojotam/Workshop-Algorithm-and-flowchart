## 1. Check Even or Odd Number

Design an algorithm and flowchart that take a number as input and
determine whether it is even or odd.

### ✔ Pseudocode

```text
START
    INPUT number
    IF number % 2 == 0 THEN
        PRINT Even
    ELSE
        PRINT Odd
    ENDIF
END
```

### ✔ Flowchart

```mermaid
flowchart TD
    A([Start]) --> I[/Get input N/]
    I --> B{N % 2 == 0 ?}
    B -->|Yes| C[/Print Even/]
    B -->|No| D[/Print Odd/]
    C --> E([End])
    D --> E([End])
```

---

## 2. Calculate Total and Average Marks

Write the algorithm and draw the flowchart for a program that inputs
marks for 3 subjects, calculates the total and average, and displays
both.

### ✔ Pseudocode

```text
START
    INPUT math
    INPUT english
    INPUT swedish
    total = math + english + swedish
    if total is a number then
        average = total / 3
        OUTPUT total
        OUTPUT average
    else
        OUTPUT "Please use numbers"

END

```
```mermaid
flowchart TB
    Start(["START"]) --> InputMath["INPUT math"]
    InputMath --> InputEnglish["INPUT english"]
    InputEnglish --> InputSwedish["INPUT swedish"]
    InputSwedish --> CalcTotal["total = math + english + swedish"]
    CalcTotal --> CheckNumber{"is total a number?"}
    CheckNumber -- yes --> CalcAverage["average = total / 3"]
    CalcAverage --> OutputTotal["OUTPUT total"]
    OutputTotal --> OutputAverage["OUTPUT average"]
    OutputAverage --> End(["END"])
    CheckNumber -- no --> OutputError["OUTPUT Please use numbers"]
    OutputError --> End
```

---

## 3. Display Multiplication Table

Create an algorithm and flowchart that input a number and display its
multiplication table from 1 to 10 using a loop.

```text
START
    INPUT MultiNumber
    If MultiNumber = number then
        for i = 1 to 10
            Result = MultiNumber * i
            OUTPUT Result
    Else
        OUTPUT "Please use numbers"

END
```
```mermaid
flowchart TB
    START(["START"]) --> INPUT["Input: MultiNumber"]
    INPUT --> CHECK{"MultiNumber = number?"}
    CHECK -- Yes --> LOOP["for i = 1 to 10"]
    LOOP --> CALC["Result = MultiNumber * i"]
    CALC --> OUTPUT1["OUTPUT Result"]
    CHECK -- No --> OUTPUT2@{ label: "OUTPUT 'Please use numbers'" }
    OUTPUT2 --> END(["END"])
    OUTPUT1 --> n1["is i &lt; 10?"]
    n1 -- Yes --> LOOP
    n1 -- No --> END
```

---

## 4. Positive, Negative, or Zero Check

Write the algorithm and flowchart to input a number and display whether
it is positive, negative, or zero.

```text
START
    Input NumberCheck
    If NumberCheck is number Then
        If NumberCheck = 0 Then
            OUTPUT "Number is 0"
        Else If NumberCheck > 0
                OUTPUT "Number is positive"
        Else
                OUTPUT "Number is negative
    Else
        OUTPUT "Please input a Number"
END

```
```mermaid
flowchart TD
    Start([START])
    Input[Input NumberCheck]
    IsNumber{Is NumberCheck<br/>a number?}
    IsZero{NumberCheck = 0?}
    IsPositive{NumberCheck > 0?}
    OutputZero[OUTPUT 'Number is 0']
    OutputPositive[OUTPUT 'Number is positive']
    OutputNegative[OUTPUT 'Number is negative']
    OutputInvalid[OUTPUT 'Please input a Number']
    End([END])
    
    Start --> Input
    Input --> IsNumber
    IsNumber -->|Yes| IsZero
    IsNumber -->|No| OutputInvalid
    IsZero -->|Yes| OutputZero
    IsZero -->|No| IsPositive
    IsPositive -->|Yes| OutputPositive
    IsPositive -->|No| OutputNegative
    OutputZero --> End
    OutputPositive --> End
    OutputNegative --> End
    OutputInvalid --> End

    

```
---

## 5. Simple Interest Calculator

Create an algorithm and flowchart for a program that calculates simple
interest using the formula:

**SI = (P × R × T) / 100**

- **P = Principal** → original amount of money
- **R = Rate of Interest** → percentage per year
- **T = Time** → number of years

```text
START
    INPUT P
    INPUT R
    INPUT T
    IF P AND R AND T is a number Then
        SI = (P * R * T) / 100
        OUTPUT SI
    Else 
        OUTPUT "Only use numeric values"
END
```
```mermaid
flowchart TD
    START([START])
    inputP[INPUT P]
    inputR[INPUT R]
    inputT[INPUT T]
    checkCondition{P AND R AND T<br/>is a number?}
    calculate[SI = P * R * T / 100]
    outputSI[OUTPUT SI]
    outputError[OUTPUT Only use numeric values]
    END1([END])
    
    START --> inputP
    inputP --> inputR
    inputR --> inputT
    inputT --> checkCondition
    checkCondition -->|Yes| calculate
    calculate --> outputSI
    outputSI --> END1
    checkCondition -->|No| outputError
    outputError --> END1
```
---

## 6. Average Temperature Calculation

Write the algorithm and draw the flowchart for a program that takes the
temperature of 7 days, finds the average temperature, and displays it.

```text
START
    Total = 0
    For i = 1 to 7
        INPUT temp
        Total = Total + temp
    END For
    Average = Total / 7
    OUTPUT Average
END
```
```mermaid
flowchart TD
    Start([Start]) --> Total[Total = 0]
    Total --> ForInit["For i = 1 to 7"]
    ForInit --> Input["INPUT temp"]
    Input --> AddTotal["Total = Total + temp"]
    AddTotal --> ForCheck{"i = 7?"}
    ForCheck -->|No| Input
    ForCheck -->|Yes| Average["Average = Total / 7"]
    Average --> Output["OUTPUT Average"]
    Output --> End([End])
```

---

## 7. Calculate Area of a Rectangle

Create an algorithm and flowchart to input length and width, calculate
the area (**Area = Length × Width**), and display the result.

---

## 8. Determine Pass or Fail

Write the algorithm and draw the flowchart for a program that takes a
student's average marks and displays **"Pass"** if average ≥ 50,
otherwise **"Fail"**.

---

## 9. Calculate Factorial of a Number

Write the algorithm and draw the flowchart that input a number and
calculate its factorial using a loop.

---

## 10. Calculate Discount on Purchase

Write the algorithm and draw the flowchart for a program that inputs the
purchase amount and gives a **10% discount** if the amount is greater
than 1000.

---


## Optional Exercises (11–16)

## 11. Online Shopping Delivery Eligibility

Write the algorithm and draw the flowchart for a program that inputs a
customer's purchase amount and displays **"Free Delivery"** if the
amount is 500 SEK or more; otherwise display **"Delivery Charge
Applies"**.

---

## 12. Employee Salary and Bonus Calculator

Write the algorithm and draw the flowchart for a program that inputs an
employee's monthly salary and years of service, calculates a bonus of
**10%** for employees with 5 or more years of service and **5%** for
others, then displays the bonus and total salary.

---

## 13. Mobile Data Usage Monitor

Write the algorithm and draw the flowchart for a program that inputs a
user's monthly data limit and data usage, then displays whether the user
has exceeded the limit or how much data remains.

---

## 14. Login System (Maximum 3 Attempts)

Create an algorithm and flowchart for a login system that allows a user
up to 3 attempts to enter the correct password. Display **"Access
Granted"** if the password is correct; otherwise display **"Account
Locked"** after 3 failed attempts.

---

## 15. Store Checkout with Multiple Items

Write the algorithm and draw the flowchart for a program that inputs the
number of items purchased, calculates the total purchase amount using a
loop, and applies a **15% discount** if the total exceeds 5000 SEK.

---

## 16. Electricity Bill Calculator

Write the algorithm and draw the flowchart for a program that inputs the
number of electricity units consumed and calculates the total bill using
the following rates: first 100 units at 1.5 SEK per unit, next 200
units at 2.0 SEK per unit, and all remaining units at 3.0 SEK per unit.

---