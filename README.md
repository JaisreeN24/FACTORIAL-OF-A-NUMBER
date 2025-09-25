# FACTORIAL-OF-A-NUMBER
# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

---

## APPARATUS REQUIRED
- Personal computer with Keil software

---

## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**

---

## FLOWCHART
<img width="332" height="357" alt="image" src="https://github.com/user-attachments/assets/7bf86de8-a231-4277-a949-9cb9cc670d84" />



---

## PROGRAM
```asm
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END

```
OUTPUT

<img width="1171" height="513" alt="Screenshot 2025-09-25 084242" src="https://github.com/user-attachments/assets/78101a41-71f7-483e-a15a-be9a0438b5ba" />

---
MANUAL CALCULATIONS


<img width="375" height="384" alt="image" src="https://github.com/user-attachments/assets/78571b08-93ce-4613-abaf-c2481e287244" />



---

RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


