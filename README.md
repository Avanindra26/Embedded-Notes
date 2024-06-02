# Embedded-Notes
Notes Realted to Embeeded tech.

**Bitwise Operators in C**
Bitwise operators in C perform operations on the individual bits of integers. They include AND (&), OR (|), XOR (^), NOT (~), left shift (<<), and right shift (>>). These operators are commonly used for tasks like setting, clearing, and toggling specific bits, performing fast arithmetic operations, and optimizing memory usage in low-level programming and embedded systems.

**1. Bitwise AND (&)**
The bitwise AND operation is used to find the common set bits of a and b. These common set bits indicate where carries need to be added in binary addition.

Binary Representation
a = 100 (binary for 4)
b = 101 (binary for 5)


int data = a & b;

   a = 1 0 0
   b = 1 0 1  
data = 1 0 0 (4 in binary)
In this operation:

The third bit from the right: Both a and b have 1, so the result is 1 (indicating a carry).
Identifying Carry Bits
Common Set Bits: The bitwise AND operation identifies positions where both a and b have 1. These are the positions where a carry will occur in binary addition.


**2. Bitwise XOR (^)**
The bitwise XOR operation compares each corresponding bit of two integers and returns a new integer where each bit is set to 1 if the corresponding bits of the original integers are different. If the corresponding bits are the same, the bit in the resulting integer is set to 0.


a = a ^ b;

   a = 1 0 0
   b = 1 0 1
   -----------
a ^ b = 0 0 1

**3. Left Shift (<<)**
The carry bits identified need to be added to the next higher bit position in the subsequent iteration. Hence, data is shifted left by one position (data << 1).


b = data << 1;

b = data << 1 = 1000 (8) ⟶ carries shifted left
The common set bit is in the third position (from the right), indicating that there is a carry from the third position to the fourth position in binary addition.







