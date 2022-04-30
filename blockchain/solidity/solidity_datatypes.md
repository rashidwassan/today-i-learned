# Solidity Data Types

## Elementary data types

### int
    used to store integer data with the support of size specification within multiples of 8 bits.
    uint8 is of 8 bits and can store integers from 0 to 255.
    size defaults to 256bits (32 byte number).

### uint
    this is integer value which is unsigned, due to not being bound with support of negative values, it can store twice of the positive
    number values supported by int.

### address
    represents 20byte Ethereum address.
    it is of value type.
    address.balance can be used to check the balance of current account.

### arrays

- Memory arrays: Those arrays which store the data in memory. int8[] memory array;
- Storage arrays: Those arrays which store data in storage, the can be dynamic. int8[] array;
 - Static Arrays:
      - bool[10] array; static array with fix size of 10 bools.
 - Dynamic Arrays: 
      - bool[] array; dynamic array with dynamic size.
      - Cannot be initialized in memory.
      - uint8[] memory arr = [1, 2, 3]; // cannot be compiled as we can't have dynamic memory arrays.
      - uint8[] memory arr; // OK
      - arr.push(1) // error

- Push function cannot be used with a memory array.
- uint8[3] arr = [1, 2, 3]
- int8[3] arr = [1, 2, 3]; this will generate error as these elements are interpreted as uint8;
- int8[] arr = [int(1), 2, 3]; gets comipled.
- We cannot assign length to a memory array.

## Data Initializations
    int will be initialized to 0.
    bool will be initialized to false.


