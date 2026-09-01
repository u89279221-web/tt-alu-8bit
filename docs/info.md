# 8-bit ALU

## How it works

The ALU takes an 8-bit operand `A` on `ui_in`, a 4-bit operand `B` on `uio_in[3:0]`, and a 4-bit `opcode` on `uio_in[7:4]`. It performs arithmetic, bitwise logic, and shift operations, outputting an 8-bit result on `uo_out` and status flags on `uio_out`.

Supported operations:
- `0000`: Addition (A + B)
- `0001`: Subtraction (A - B)
- `0010`: Bitwise AND (A & B)
- `0011`: Bitwise OR (A | B)
- `0100`: Bitwise XOR (A ^ B)
- `0101`: Bitwise NOT (~A)
- `0110`: Shift Left Logical (A << B[2:0])
- `0111`: Shift Right Logical (A >> B[2:0])

## How to test

1. Apply operand `A` on input pins `ui_in[7:0]`.
2. Apply operand `B` (lower 4 bits) on `uio_in[3:0]`.
3. Set the operation code on `uio_in[7:4]`.
4. Observe the result on `uo_out[7:0]`.
5. Check `uio_out[7:4]` for status flags (Carry, Zero, Negative, and Overflow).
6.
