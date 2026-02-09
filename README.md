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

<img width="707" height="807" alt="image" src="https://github.com/user-attachments/assets/bd50b5d0-ee02-4e82-92b8-b274abe7a5f2" />


#### Manual Calculations

<img width="1573" height="810" alt="image" src="https://github.com/user-attachments/assets/26213136-fbe5-453a-a65e-c6d237804c89" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="814" height="559" alt="image" src="https://github.com/user-attachments/assets/3d5fcdc8-1b61-4c4e-b592-9fa25622ca57" />

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

<img width="1167" height="814" alt="image" src="https://github.com/user-attachments/assets/3636fb3d-ca74-4139-9fef-36d57f645a9f" />

#### Manual Calculations

<img width="959" height="804" alt="image" src="https://github.com/user-attachments/assets/ec20e818-fdb4-4b57-8d92-dbc370b7c14f" />

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="789" height="529" alt="image" src="https://github.com/user-attachments/assets/3f7291a7-8cdb-453f-8a62-76bea7d55eeb" />

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

<img width="1330" height="799" alt="image" src="https://github.com/user-attachments/assets/554914bb-4878-4c6c-9b66-18a2a4ec1aa7" />


#### Manual Calculations

<img width="1211" height="802" alt="image" src="https://github.com/user-attachments/assets/5c074305-89ac-4b85-a87f-d5a4414b7417" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="803" height="526" alt="image" src="https://github.com/user-attachments/assets/b0566052-b6b3-4e80-b17e-e7cf7543a0e7" />

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
<img width="1085" height="800" alt="image" src="https://github.com/user-attachments/assets/a567bae6-02db-49b9-bb63-0442e294ac12" />


#### Manual Calculations

<img width="1191" height="800" alt="image" src="https://github.com/user-attachments/assets/1037f278-fb31-4ea1-b6ad-5feeabd4f76f" />

---
## OUTPUT FROM MASM SOFTWARE
<img width="788" height="530" alt="image" src="https://github.com/user-attachments/assets/bc9ff743-7952-4556-881a-5adb6cd16e03" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

