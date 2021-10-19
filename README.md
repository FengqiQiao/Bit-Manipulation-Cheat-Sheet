# Bit-Manipulation-Cheat-Sheet (Continue Updating)

### Basics:
(AND) &  
(OR) |  
(XOR) ^  
(NOT) ~   
(LEFT SHIFT)<<   
(RIGHT SHIFT) \>>   

### Intermediate:
#### Setting Bits:
Set the nth bit of a value x to be 1:
```c
x |= (1 << n)
```  
```c
#define SET_BIT(byte, bit) ((byte) |= (1UL << (bit)))
```
#### Clearing Bits
Clear the nth bit of a value x to be 0 (we need to mask n-1 bits):
```c
x &= ~(1 << n)
```  
```c
#define CLEAR_BIT(byte, bit) ((byte) &= ~(1UL << (bit)))
```
#### Flipping Bits
Flip the bit (XOR with 1) of a value x at position n from 0 to 1, or 1 to 0:
```c
x ^= (1 << n)
```
```c
#define FLIP_BIT(byte, bit) ((byte) ^= (1UL) << (bit))
```
#### Updating Bits

#### LSB 
