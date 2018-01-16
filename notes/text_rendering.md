| Version(s) |
| ---------- |
| * Saturn |

## Description

The Saturn version uses fixed-width 16-bit codepoints for its text. Text is rendered one codepoint at a time, until a line is complete. The text rendering loop works roughly like this:

* Set register 14 to a pointer to the beginning of a string.
* Read a word out of RAM into register 2.
* Compare if the value is equal to or greater than 0F00 (??)
* If false, add two bytes to the pointer at register 14, and repeat the read.
* Compare if the value is equal to FFFF to detect the end of dialogue
* If dialogue isn't over, jump to a comparison against 0800 (??).
* If comparison is false, jump to the first step and continue looping.

## The text-rendering loop

| RAM address | Instruction | Hex value | Notes |
| -------- | -------------- | ---- | ------------------------------------|
| 060BAA54 | mov.w @r14, r2 | 62E1 | two bytes are copied from r14 to r2 |
| 060BAA56 | extu.w r2. r2 | 622D | |
| 060BAA58 | cmp/ge r12, r2 | 32C3 | r12 is 0F00 |
| 060BAA5A | bf to 060BAA60 | 8B01 | |
| | | |
| 060BAA60 | add #0x02, r14 | 7E01 | edit the byte at 060BAA61 from 0x02 to 0x01 |
| 060BAA62 | mov.w @r14, r2 | 62E1 | two bytes are copied from r14 to r2 |
| 060BAA64 | extu.w r2. r2 | 622D | word in r2 is zero-extended |
| 060BAA66 | cmp/eq r11, r2 | 32B0 | compare r2 to r11 (which is 0000FFFF) to see if we hit the end of a text box |
| 060BAA68 | bf to 060BAA3C | BB01 | |
| | | |
| 060BAA3C | mov.w @r14, r2 | 62E1 | two bytes are copied from r14 to r2 |
| 060BAA3E | extu.w r2. r2 | 622D | word in r2 is zero-extended |
| 060BAA40 | cmp/ge r13, r2 | 32D3 | r13 is 0800 |
| 060BAA42 | bt to 060BAA54 | 8907 | |
| 060BAA5A | bf to 060BAA60?| 8B01 | Not sure if this is actually the associated bf |
