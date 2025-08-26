# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|   1200  - 12            |   1204  - 24             |
|   1201  - 34            |   1205  - 68             |
|   1202  - 12            |   1206  - 00             |
|   1203  - 34            |                          |
    

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-08-24 at 19 29 31_5a071400](https://github.com/user-attachments/assets/aaf9ee6b-ea78-4355-a3f7-40d805a62fea)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="643" height="207" alt="Screenshot 2025-08-24 171554" src="https://github.com/user-attachments/assets/6a2443de-d9bc-4ac5-80cd-e2ec62721859" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program

<img width="599" height="366" alt="Screenshot 2025-08-24 173304" src="https://github.com/user-attachments/assets/31cfb6f9-503b-45f9-8ac6-d2e8736fc73a" />




#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|   1200  - 12            |   1204  - 00             |
|   1201  - 34            |   1205  - 00             |
|   1202  - 12            |                          |
|   1203  - 34            |                          |



#### Manual Calculations

(Add your calculation here)![WhatsApp Image 2025-08-24 at 19 29 30_6a922e45](https://github.com/user-attachments/assets/7361a444-fef8-437c-8124-f994b62d9e02)

-----


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="655" height="194" alt="Screenshot 2025-08-24 173200" src="https://github.com/user-attachments/assets/282200bb-dab3-43c7-9a86-e7a9b5a8843a" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| ----------------------- | ------------------------ |
|   1200  - 12            |   1204  - 44             |
|   1201  - 34            |   1205  - 51             |
|   1202  - 12            |    1206  - 97            |
|   1203  - 34            |    1207   0A             |

#### Manual Calculations

![WhatsApp Image 2025-08-26 at 05 55 17_0e441b4a](https://github.com/user-attachments/assets/c3182047-469a-40ae-a2f4-c729c3ef3212)

(Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="618" height="401" alt="Screenshot 2025-08-20 161307" src="https://github.com/user-attachments/assets/ab2e3d62-5388-4925-8548-330534a842d9" />

<img width="615" height="210" alt="Screenshot 2025-08-20 160833" src="https://github.com/user-attachments/assets/ba97b7d9-9a00-4099-a99c-a9248a9bfde5" />



## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
