# MULTIPLICATION INSTRUCTIONS AND FLAG ANALYSIS

## Example 1: 8-bit Multiplication

### Flag Analysis

| Flag | Status | Explanation |
|---|---|---|
| CF | Cleared (0) | AH is zero, meaning the product fits within 8 bits. |
| OF | Cleared (0) | The upper 8 bits of the product are zero. |
| PF | Undefined | MUL does not define the Parity Flag. |
| AF | Undefined | MUL does not define the Auxiliary Carry Flag. |
| ZF | Undefined | MUL does not define the Zero Flag. |
| SF | Undefined | MUL does not define the Sign Flag. |
| IF | Unchanged | MUL does not modify the Interrupt Enable Flag. |

## Example 2: 16-bit Multiplication

### Flag Analysis

| Flag | Status | Explanation |
|---|---|---|
| CF | Set (1) | DX is nonzero, meaning the product does not fit within 16 bits. |
| OF | Set (1) | The upper 16 bits of the product are nonzero. |
| PF | Undefined | MUL does not define the Parity Flag. |
| AF | Undefined | MUL does not define the Auxiliary Carry Flag. |
| ZF | Undefined | MUL does not define the Zero Flag. |
| SF | Undefined | MUL does not define the Sign Flag. |
| IF | Unchanged | MUL does not modify the Interrupt Enable Flag. |
