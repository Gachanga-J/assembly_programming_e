# Addition Instructions and Flag Analysis

## Example 1: 8-bit Addition

| Flag | Status | Explanation |
|---|---|---|
| CF | Cleared (0) | No carry was generated beyond the 8-bit result. |
| PF | Set (1) | The binary result (10000010) contains two 1s, which is even parity. |
| AF | Set (1) | Adding the lower nibbles (8 + A) produces a carry from bit 3 to bit 4. |
| ZF | Cleared (0) | The result is 130, not zero. |
| SF | Set (1) | The most significant bit of the result is 1. |
| OF | Set (1) | Both operands are positive signed numbers, but 130 exceeds the maximum signed 8-bit value of 127. |

## Example 2: 16-bit Addition

| Flag | Status | Explanation |
|---|---|---|
| CF | Cleared (0) | No carry was generated beyond the 16-bit result. |
| PF | Cleared (0) | The lower byte (F4H = 11110100) contains five 1s, giving odd parity. |
| AF | Cleared (0) | Adding the lower nibbles (0 + 4) produces no auxiliary carry. |
| ZF | Cleared (0) | The result is 32500, not zero. |
| SF | Cleared (0) | The most significant bit of the 16-bit result is 0. |
| OF | Cleared (0) | The result is within the signed 16-bit range of -32768 to +32767. |
