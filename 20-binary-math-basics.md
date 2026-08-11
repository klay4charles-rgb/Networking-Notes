# Binary Math –

## 1. What is Binary?
Binary is a base-2 number system used by computers.
It only uses two digits: **0 and 1**

- 0 = OFF
- 1 = ON

---

## 2. Binary Place Values (Powers of 2)

Each bit represents a power of 2:

| Bit Position | Value |
|-------------|------|
| 2^7 | 128 |
| 2^6 | 64  |
| 2^5 | 32  |
| 2^4 | 16  |
| 2^3 | 8   |
| 2^2 | 4   |
| 2^1 | 2   |
| 2^0 | 1   |

### Example (8-bit):
11111111 = 255  
10000000 = 128  

---

## 3. Decimal → Binary Conversion

### Method: Repeated Division by 2

Steps:
1. Divide number by 2
2. Record remainder (0 or 1)
3. Keep dividing until result is 0
4. Read remainders from bottom to top

### Example: 13 → Binary

13 ÷ 2 = 6 remainder 1  
6 ÷ 2 = 3 remainder 0  
3 ÷ 2 = 1 remainder 1  
1 ÷ 2 = 0 remainder 1  

👉 Result: **1101**

---

## 4. Binary → Decimal Conversion

### Method: Sum of Powers of 2

Steps:
1. Write binary number
2. Assign powers of 2 from right to left
3. Add values where bit = 1

### Example: 1101 → Decimal

- 1 × 8 = 8  
- 1 × 4 = 4  
- 0 × 2 = 0  
- 1 × 1 = 1  

👉 8 + 4 + 1 = **13**

---

## 5. Quick Tips

- Rightmost bit = 2^0
- Each position to the left doubles the value
- Binary numbers only use 0 and 1
- Always align bits properly when converting

---

## 6. Common Values

| Decimal | Binary   |
|----------|----------|
| 1        | 0001     |
| 2        | 0010     |
| 4        | 0100     |
| 8        | 1000     |
| 10       | 1010     |
| 16       | 10000    |
| 32       | 100000   |
