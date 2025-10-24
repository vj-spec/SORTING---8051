# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**
```
ORG 0000H 
MOV R7,#4
LOOP1:MOV R0,#40H 
MOV R6,#04
LOOP: MOV A,@R0 
INC R0
MOV 50H,@R0 
CJNE A,50H,NEXT 
SJMP DOWN 
NEXT:JNC DOWN 
MOV @R0,A
DEC R0
MOV @R0,50H 
DOWN:DJNZ R6,LOOP 
DJNZ R7,LOOP1
END
```

**OUTPUT:**
![WhatsApp Image 2025-10-24 at 07 15 05_6fef74e3](https://github.com/user-attachments/assets/2243995b-3dfa-4cdb-8b87-dac4ab64ace7)


**MEMORY WINDOW:**

Before execution: D:0x40H:
<img width="957" height="338" alt="image" src="https://github.com/user-attachments/assets/3f7d6337-bc04-498a-9553-82854781368e" />

After execution: D:0x40H:
<img width="957" height="336" alt="image" src="https://github.com/user-attachments/assets/99f45551-c75a-42aa-9bc5-182cf41634ba" />



**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**
```
ORG 0000H 
MOV R7,#4
LOOP1:MOV R0,#40H
MOV R6,#04
LOOP: MOV A,@R0
INC R0
MOV 50H,@R0 
CJNE A,50H,NEXT
SJMP DOWN 
NEXT:JC DOWN
MOV @R0,A
DEC R0
MOV @R0,50H 
DOWN:DJNZ R6,LOOP 
DJNZ R7,LOOP1
END
```
**OUTPUT:**
![WhatsApp Image 2025-10-24 at 07 21 15_ea07c1bb](https://github.com/user-attachments/assets/cc3a35f6-05e5-46b2-9d9c-b394ad8041d6)


**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
<img width="952" height="272" alt="image" src="https://github.com/user-attachments/assets/112ca933-1d38-4670-8e81-3bcc2a5f8513" />

After execution:
D:0x40H:
<img width="957" height="277" alt="image" src="https://github.com/user-attachments/assets/9e3a3e1a-df98-4e2f-a826-be2cec128907" />

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

