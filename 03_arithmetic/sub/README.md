# SUBTRACTION INSTRUCTIONS AND FLAG ANALYSIS

## Example 1: 8-bit Subtraction

### Flag Analysis

| Flag | Status | Explanation |
|---|---|---|
| CF | Set (1) | 50 is smaller than 80, so an unsigned borrow is required. |
| PF | Cleared (0) | E2H = 11100010₂ contains three 1s, which is odd parity. |
| AF | Cleared (0) | The lower nibbles are 2H - 0H, so no borrow occurs from bit 4. |
| ZF | Cleared (0) | The result E2H is not zero. |
| SF | Set (1) | The most significant bit of E2H is 1, so the result has a negative sign. |
| OF | Set (1) | 50 is positive and 80H represents a negative signed value (-128 to -1), and the subtraction produces a signed result that cannot be represented correctly in 8 bits. |
| IF | Unchanged | SUB does not modify the Interrupt Enable Flag. |

---

## Example 2: 16-bit Subtraction

### Flag Analysis

| Flag | Status | Explanation |
|---|---|---|
| CF | Set (1) | 1000 is smaller than 2000, so an unsigned borrow is required. |
| PF | Set (1) | The lower byte of FC18H is 18H = 00011000₂, which contains two 1s, giving even parity. |
| AF | Cleared (0) | The lower nibbles are 8H - 0H, so no borrow occurs from bit 4. |
| ZF | Cleared (0) | The result FC18H is not zero. |
| SF | Set (1) | The most significant bit of the 16-bit result is 1, indicating a negative result. |
| OF | Cleared (0) | Both operands are positive and the result (-1000) is within the signed 16-bit range of -32768 to +32767. |
| IF | Unchanged | SUB does not modify the Interrupt Enable Flag. |
