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
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200:12           |     1204:24              |
|       1201:34           |     1205:68              |
|       1202:12           |                          |
|       1203:34           |                          |

                   

#### Manual Calculations

<img width="976" height="719" alt="image" src="https://github.com/user-attachments/assets/d7e1a1dd-c0d0-4aa3-b65f-8c44d05d21dd" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="818" height="549" alt="Screenshot 2026-05-14 at 3 37 48 PM" src="https://github.com/user-attachments/assets/845bd520-b393-4e58-be2a-b5e96a10ffd1" />


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
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
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
|   1200:12               |  1204:00                 |
|   1201:34               |  1205:00                 |
|   1202:12               |                          |
|   1203:34               |                          |

#### Manual Calculations
 <img width="1308" height="729" alt="image" src="https://github.com/user-attachments/assets/abd6cb79-3bb1-4a48-97f2-97333323fc4a" />





## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="843" height="541" alt="Screenshot 2026-05-14 at 3 44 10 PM" src="https://github.com/user-attachments/assets/da77ccc6-5551-499b-8b08-3fba43ae6985" />


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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1200:12             |   1204:44                |
|     1201:34             |   1205:51                |
|     1202:12             |   1206:97                |
|     1203:34             |   1207:0A                |

#### Manual Calculations

<img width="1439" height="896" alt="image" src="https://github.com/user-attachments/assets/03133bc0-ddb6-4ec6-8f65-2b60d9777601" />


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="696" height="268" alt="Screenshot 2026-05-14 at 3 48 04 PM" src="https://github.com/user-attachments/assets/eaf89c3a-640c-488e-b7a4-628cea267e5b" />


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
|    1200:12              |                          |
|    1201:34              |     1204:01              |
|    1202:12              |     1205:00              |
|    1203:34              |     1206:00              |


#### Manual Calculations
<img width="1274" height="637" alt="image" src="https://github.com/user-attachments/assets/bce5021d-54ef-4a86-97c0-7557d99cbc7b" />

## OUTPUT FROM MASM SOFTWARE
<img width="862" height="489" alt="Screenshot 2026-05-14 at 3 51 16 PM" src="https://github.com/user-attachments/assets/ff5b1347-d709-4595-983d-ea49b4abf10f" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

