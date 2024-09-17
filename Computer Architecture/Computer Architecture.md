# Computer Architecture Notes

## Computer Basics

### Main Components
- **Memory Subsystem**
- **Input/Output Subsystem**
- **Central Processing Unit (CPU)**

### Program Execution
1. **Input**: Data is read from the disk.
2. **Main Memory**: Program code is loaded from the disk.
3. **CPU**: Executes the program code.
4. **Output**: Results are produced.

## Computer Architecture

### Structure of a Computer
1. **Structure of a Computer**
2. **Instruction Set of a Computer**
3. **Designing a Computer**

#### Structure of a Computer
- **Output**
- **Instruction Set**
  - To operate a computer, instructions are given in binary form.
  - Examples: Intel, ARM, MIPS

### Instruction Set
- **Instructions**: Commands in the computer's language (e.g., ADD, LDA, MOV).
- **Machine Language**: Binary instructions (e.g., `0011 1110 0000 0101` for adding a value of 5).
- **Assembly Language**: Human-readable form (e.g., `ADI 5`).

#### Sample Instruction Set

| Binary Opcode | Mnemonic | Description                              |
|---------------|----------|------------------------------------------|
| 1000 0111     | 87       | ADD A: Add the contents of register A to the accumulator |
| 0011 1010     | 3A       | LDA: Load data stored in the given memory address |
| 0111 1001     | 79       | MOVAC: Move data from register A to C    |
| 1100 0011     | C3       | JMP: Jump to instruction in specified memory address |
| 1100 0001     | C1       | POP B: Pop from stack and copy to memory register B + C |

### Designing a Computer
- **Performance Requirements**
- **Interconnections between Parts**
- **Instruction Set Definition**
- **Logical Implementation** (e.g., CPU/memory design)

## Computer Performance

### Key Metrics
- **Response Time**: Time taken to complete a task.
- **Throughput**: Total amount of work done in a given time.

#### Performance Improvement Scenarios
1. **Replacing a Processor**: Improves both response time and throughput.
2. **Adding Multiple Processors**: Generally improves both response time and throughput.

### CPU Performance Calculation
- **CPU Execution Time**:
  \[
  \text{Performance} = \frac{1}{\text{CPU Execution Time}}
  \]

#### Example Calculation
- **Computer A**:
  - Clock rate: 2 GHz
  - Time: 10 seconds
  - Cycles: \(2 \times 10^9 \times 10 = 20 \times 10^9\) cycles

- **Computer B**:
  - Time: 6 seconds
  - Cycles: \(1.2 \times 20 \times 10^9 = 24 \times 10^9\)
  - Clock rate: \(\frac{24 \times 10^9}{6} = 4 \times 10^9\) cycles/second or 4 GHz

### Clock Cycle
- **Clock Cycle**: Time to complete one cycle (e.g., 0.25 ns = \(0.25 \times 10^{-9}\) seconds).
- **Clock Rate**: Number of cycles per second.

## Computer History

### Generations of Computers

| Generation | Period       | Details                                       |
|-------------|--------------|-----------------------------------------------|
| 0th          | 1642-1945    | Mechanical computers (e.g., Difference Engine, Analytical Engine, Konrad Zuse’s machines) |
| 1st          | 1945-1955    | Vacuum tubes (e.g., COLOSSUS, ENIAC)         |
| 2nd          | 1955-1965    | Transistors (e.g., PDP-1, CDC 6600, Cray Supercomputers) |
| 3rd          | 1965-1980    | Integrated Circuits (e.g., IBM System/360 series) |
| 4th          | 1980-Ongoing | VLSI (e.g., IBM PCs, Apple Macintosh)        |
| 5th          | 1990s-Onwards| Low power and invisible computers (e.g., PDAs, Smartphones) |

### Reduction in Transistor Size

![Transistor Size Reduction](https://example.com/transistor-size.png)

| Year | Size (nm) |
|------|-----------|
| 2000 | 180       |
| 2002 | 130       |
| 2004 | 90        |
| 2006 | 65        |
| 2008 | 45        |
| 2010 | 32        |
| 2012 | 22        |
| 2014 | 14        |
| 2016 | 10        |
| 2018 | 7         |
| 2020 | 5         |

### Moore's Law

Moore's Law states that the number of transistors on a microchip doubles approximately every two years.

#### Historical Data

| Processor       | Year | Transistors  |
|-----------------|------|--------------|
| 4004            | 1971 | 2,300        |
| 8008            | 1972 | 3,500        |
| 8080            | 1974 | 6,000        |
| 8086            | 1978 | 29,000       |
| 8088            | 1979 | 29,000       |
| 80286           | 1982 | 134,000      |
| 80386           | 1985 | 275,000      |
| 80486           | 1989 | 1.2M         |
| Pentium         | 1993 | 3.1M         |
| Pentium Pro     | 1995 | 5.5M         |
| Pentium II      | 1997 | 7.5M         |
| Pentium III     | 1999 | 9.5M         |
| Pentium 4       | 2000 | 42M          |
| Core Duo        | 2006 | 152M         |
| Core i7         | 2011 | 1160M        |

## Computer Organization vs. Computer Architecture

### Computer Organization
- **Physical Aspects**
- **Microarchitecture or Low-level Architecture**
- **Implementation Details**

### Computer Architecture
- **Logical Aspects**
- **High-level Architecture**
- **Instruction Set, Addressing Mode, Data Types**

## Fetch-Decode-Execute Cycle

### Steps
1. **Fetch**: Retrieve the instruction from memory.
2. **Decode**: Interpret the instruction.
3. **Execute**: Perform the instruction.
4. **Store Results**: Save the result to memory.

### Diagram

```plaintext
[ Fetch ] --> [ Decode ] --> [ Execute ] --> [ Store Results ]



Certainly! Below are the rewritten notes with diagrams included in Markdown format.

---

## The ‘Bus’ Concept

### Computer Bus

- **Computer Bus**: A communication link (set of wires) used inside a computer to send data, addresses, control signals, and power to various hardware components.
- **Function**: Buses connect various hardware components to each other.
- **Main Bus Types**:
  - **Address Bus**: Used for specifying memory addresses for reading or writing of data. (Unidirectional)
  - **Data Bus**: Specifies data to be written or contains data that was read. (Bidirectional)
  - **Control Bus**: Used for passing control signals. (Bidirectional)
- **System Bus**: Combines Address Bus + Data Bus + Control Bus.

#### How the System Bus Works

- **Writing Data**:
  - **CPU** wants to write a value of `0` to memory location `125`.
  - **Address Bus** specifies the address `125`.
  - **Data Bus** carries the data `0`.
  - **Control Bus** signals a write operation.

- **Reading Data**:
  - **CPU** wants to read data from memory location `125`.
  - **Address Bus** specifies the address `125`.
  - **Control Bus** signals a read operation.
  - **Data Bus** carries the data read from memory location `125`.

### von Neumann vs. Harvard Architecture

#### von Neumann Architecture

- **Characteristics**:
  - Single memory for data and instructions.
  - Single bus.
  - Simple and inexpensive.
  - Cannot perform simultaneous multiple memory fetches.
  - Known for the von Neumann bottleneck due to the separation of memory and data.

#### Harvard Architecture

- **Characteristics**:
  - Separate memory and separate buses for data and instructions.
  - Multi-bus system.
  - Complex and expensive.
  - Can perform simultaneous two memory fetches.

**Diagram: von Neumann vs. Harvard Architecture**

```plaintext
von Neumann Architecture:
   +---------------------+
   |                     |
   |  Main Memory        |
   |  (Data & Instructions) |
   |                     |
   +--------+------------+
            |
            |
            v
   +--------+------------+
   |                     |
   |         CPU          |
   |  +-------------+    |
   |  | Control Unit|    |
   |  | ALU         |    |
   |  | Registers   |    |
   |  +-------------+    |
   |                     |
   +---------------------+
            |
            |
            v
   +---------------------+
   |                     |
   |     I/O Devices     |
   |  (Keyboard, Display, etc.) |
   |                     |
   +---------------------+

Harvard Architecture:
   +---------------------+        +---------------------+
   |                     |        |                     |
   |   Data Memory       |        |  Instruction Memory |
   |                     |        |                     |
   +--------+------------+        +--------+------------+
            |                             |
            |                             |
            v                             v
   +--------+------------+        +--------+------------+
   |                     |        |                     |
   |         CPU          |        |         CPU          |
   |  +-------------+    |        |  +-------------+    |
   |  | Control Unit|    |        |  | Control Unit|    |
   |  | ALU         |    |        |  | ALU         |    |
   |  | Registers   |    |        |  | Registers   |    |
   |  +-------------+    |        |  +-------------+    |
   |                     |        |                     |
   +--------+------------+        +--------+------------+
            |                             |
            |                             |
            v                             v
   +---------------------+        +---------------------+
   |                     |        |                     |
   |     I/O Devices     |        |     I/O Devices     |
   |  (Keyboard, Display, etc.) |   |  (Keyboard, Display, etc.) |
   |                     |        |                     |
   +---------------------+        +---------------------+
```

### PCI Express

- **Earlier**: Each component/device was connected using separate wires (Point-to-Point connection).
- **Now**: A common bridge connects various devices (Multi-Point connection).
- **PCI Express**: Modern system bus technique.
  - **Components**:
    - CPU, memory, and cache are connected to a bridge chip.
    - A switch connects to the bridge.
    - Each I/O chip has a dedicated point-to-point connection to the switch.
    - Each connection consists of a pair of unidirectional channels (one to the switch and one from it).
  - **Function**: All devices are treated equally and work like a packet-switching network.

**Diagram: PCI Express Architecture**

```plaintext
   +---------------------+
   |                     |
   |         CPU         |
   |                     |
   +--------+------------+
            |
            |
            v
   +---------------------+
   |                     |
   |      Bridge Chip    |
   |                     |
   +--------+------------+
            |
            |
            v
   +---------------------+
   |                     |
   |       Switch        |
   |                     |
   +--------+------------+
      |      |      |      |
      |      |      |      |
      v      v      v      v
   +---+  +---+  +---+  +---+
   | I/O|  | I/O|  | I/O|  | I/O|
   | Chip|  | Chip|  | Chip|  | Chip|
   +---+  +---+  +---+  +---+
```

### CPU Organization

- **CPU**: Comprises Control Unit (CU), Arithmetic and Logical Unit (ALU), and Registers.
  - **Control Unit (CU)**: Directs operations of the CPU.
  - **ALU (Arithmetic and Logical Unit)**: Performs arithmetic and logical operations.
  - **Registers**: Fast memory inside the CPU used for operations.

**Diagram: Basic CPU Organization**

```plaintext
   +---------------------+
   |                     |
   |         CPU         |
   |  +-------------+    |
   |  | Control Unit|    |
   |  | ALU         |    |
   |  | Registers   |    |
   |  +-------------+    |
   |                     |
   +---------------------+
            |
            |
            v
   +---------------------+
   |                     |
   |      I/O Devices    |
   |                     |
   +---------------------+
```

### Registers

- **Purpose**: Perform all arithmetic and logical operations.
- **Intel CPU Registers**:
  - **AX**: Accumulator Register
  - **BX**: Base Address Register
  - **CX**: Counting Register
  - **DX**: Data Register
  - **IP**: Instruction Pointer (points to the next instruction)
  - **Flags**: Contains results of a comparison.

**Diagram: x86 Registers**

```plaintext
   +---------------------+
   |       AX            |
   |  +-----+ +-----+    |
   |  | AH  | | AL  |    |
   +-----+ +-----+      |
   +---------------------+
   |       BX            |
   |  +-----+ +-----+    |
   |  | BH  | | BL  |    |
   +-----+ +-----+      |
   +---------------------+
   |       CX            |
   |  +-----+ +-----+    |
   |  | CH  | | CL  |    |
   +-----+ +-----+      |
   +---------------------+
   |       DX            |
   |  +-----+ +-----+    |
   |  | DH  | | DL  |    |
   +-----+ +-----+      |
   +---------------------+
   |  IP (Instruction Pointer) |
   +---------------------+
   |  Flags              |
   +---------------------+
```

### Arithmetic and Logical Unit (ALU)

- **Function**: Performs most of the operations like arithmetic (e.g., addition) and logical operations.

**Diagram: ALU Operation**

```plaintext
   +-------------------+
   |      Input A      |
   +-------------------+
            |
            v
   +-------------------+
   |        ALU        |
   |  Operation: ADD   |
   |  (e.g., AX + 5)   |
   +-------------------+
            |
            v
   +-------------------+
   |      Output       |
   |   (Result in AX)  |
   +-------------------+
```

### Control Unit (CU)

- **Components**:
  - **Instruction Pointer (IP)**: Contains the address of the next instruction.
  - **Instruction Register (IR)**: Holds the current instruction.
- **Function**:
  - Fetch the instruction code using IP.
  - Decode the instruction and execute it.
  - Increment IP to point to the next instruction.

**Diagram: Control Unit Operation**

```plaintext
   +---------------------+
   |                     |
   |  Instruction Pointer (IP) |
   +---------------------+
            |
            v
   +---------------------+
   |  Fetch Instruction  |
   |    from Memory      |
   +---------------------+
            |
            v
   +---------------------+
   |   Instruction Register (IR) |
   +---------------------+
            |
            v
   +---------------------+
   |   Decode & Execute  |
   |    Instruction       |
   +---------------------+
            |
            v
   +---------------------+
   |   Increment IP



   ### Addressing Modes

**Addressing Modes Overview**
- **Definition**: Addressing mode determines how to identify the operands for instructions.
- **Types**: Register, Immediate, Direct, Indirect, and Indexed.
- **Benefits**: Offers flexibility for operands to be in registers, memory, or in locations pointed to by other memory locations.
- **Drawback**: Adds complexity to instructions.

**Register Addressing Mode**
- **Definition**: Operands are located in CPU registers.
- **Example**: `add ax, bx` adds the contents of registers `ax` and `bx`.
- **Advantages**: Fastest mode due to direct register access.
- **Limitations**: Number of operands is constrained by the number of available registers.
- **Example Program**:
  ```assembly
  mov ax, 03h
  mov bx, 05h
  add ax, bx
  ```

**Immediate Addressing Mode**
- **Definition**: Operand is a constant value.
- **Example**: `add ax, 25` adds the constant value `25` to register `ax`.
- **Advantages**: No memory access required.
- **Limitations**: Limited use for immediate values.
- **Example Program**:
  ```assembly
  mov ax, 03h
  add ax, 05h
  ```

**Direct Addressing Mode**
- **Definition**: Uses the direct memory address of the operand.
- **Example**: `mov ax, [1000]` loads the value at memory address `1000` into register `ax`.
- **Advantages**: Simple and straightforward.
- **Limitations**: Limited by addressable memory space.
- **Example Program**:
  ```assembly
  mov ax, 03h
  mov [1000h], 05h
  add ax, [1000h]
  ```

**Indirect Addressing Mode**
- **Definition**: Operand is accessed via a memory address contained in a register.
- **Example**: `mov ax, [bx]` loads the value from the memory address held in register `bx` into `ax`.
- **Advantages**: Provides flexibility in accessing different memory locations.
- **Limitations**: More complex and slower due to additional memory access.
- **Example Program**:
  ```assembly
  mov ax, 03h
  mov [1000h], 05h
  mov bx, 1000h
  add ax, [bx]
  ```

**Indexed Addressing Mode**
- **Definition**: Uses an address calculated by adding a base address to an index value.
- **Example**: `mov ax, [1000 + bx]` loads the value from the address computed by adding `bx` to `1000`.
- **Advantages**: Useful for accessing arrays, pointers, and data structures.
- **Example Program**:
  ```assembly
  mov ax, 1000h
  mov bx, 02h
  add ax, [1000h + bx]
  ```

---

### Number Systems and Data Representation

**Number Systems Overview**
- **Decimal System**: Base-10 system using digits 0-9.
- **Binary System**: Base-2 system using digits 0 and 1. Preferred for computers due to its simplicity in electronic circuitry.

**Decimal Odometer**
- **Operation**: Demonstrates how decimal numbers increment and reset with carry.
- **Example**: After running for 1 kilometer, a car's odometer displays `00001`. After 10 kilometers, it shows `00010`.

**Binary Odometer**
- **Operation**: Demonstrates how binary numbers increment and reset with carry.
- **Example**: Starting at `0000`, after 1 kilometer it shows `0001`. After 2 kilometers, it shows `0010`. This continues with binary increments.

**Binary Numbers**
- **Definition**: Strings of 0s and 1s representing numbers in binary form.
- **Conversion**: For instance, decimal 42 is `101010` in binary.

**Bit**
- **Definition**: Short for binary digit, representing a single 0 or 1.
- **Examples**: `1010` is a 4-bit number, `100100` is a 6-bit number.

**Decimal Weights**
- **Definition**: Positional values of decimal digits (units, tens, hundreds, etc.).
- **Example**: Decimal number `57034` is evaluated as `(5 x 10^4) + (7 x 10^3) + (0 x 10^2) + (3 x 10^1) + (4 x 10^0)`.

**Binary Weights**
- **Definition**: Positional values of binary digits, which are powers of 2.
- **Example**: Binary number `11001` is evaluated as `(1 x 2^4) + (1 x 2^3) + (0 x 2^2) + (0 x 2^1) + (1 x 2^0)`.

**Conversion Examples**
- **Binary to Decimal**: Convert `11001100` to decimal yields `204`.
- **Decimal to Binary**: Convert `125` to binary results in `1111101`.
- **Hexadecimal Conversion**:
  - **Hexadecimal to Decimal**: `F8E6` converts to `63718`.
  - **Decimal to Hexadecimal**: `3479` converts to `0x4B7`.

**Key Terminology**
- **Bit**: A single binary digit (0 or 1).
- **Nibble**: 4 bits (half a byte).
- **Byte**: 8 bits.
- **Word**: 16 bits (2 bytes).

**Hexadecimal Numbers**
- **Definition**: Base-16 number system using digits 0-9 and letters A-F.
- **Example**: `10101101011` in binary is `56B` in hexadecimal.

**BCD Numbers**
- **Definition**: Binary-Coded Decimal where each decimal digit is represented by a 4-bit binary number.
- **Example**: Decimal `2945` in BCD is `0010 1001 0100 0101`.

**ASCII Code**
- **Definition**: A character encoding standard that maps characters to binary values.
- **Historical Note**: Originally 7-bit, now often 8-bit in extended ASCII.

**Conversion Summary**
- **Binary-to-Decimal**: Use the 8-4-2-1 method or multiplication of powers of 2.
- **Decimal-to-Binary**: Divide by 2, record remainders, reverse them.
- **Hex-to-Decimal**: Multiply hexadecimal digits by powers of 16.
- **Decimal-to-Hex**: Divide by 16, record remainders, reverse them.
- **Binary-to-Hex**: Convert each 4-bit binary group to its hexadecimal equivalent.
- **Hex-to-Binary**: Convert each hexadecimal digit to its 4-bit binary equivalent.



Here's a summary and some additional context on the topics covered:

### Unicode and Character Encoding

1. **Unicode**:
   - **Definition**: A universal character encoding standard designed to include characters from many writing systems.
   - **Character Count**: Includes about 100,000 characters.
   - **Encoding Size**: Typically uses up to 4 bytes (32 bits) per character, allowing it to represent a wide variety of characters.
   - **ASCII**: Uses 1 byte (8 bits) for each character, which limits its range to 128 characters, including English letters, digits, and basic punctuation.

### Binary Arithmetic

1. **Binary Addition**:
   - **Rules**:
     - 0 + 0 = 0
     - 0 + 1 = 1
     - 1 + 0 = 1
     - 1 + 1 = 10 (carry 1)
     - 1 + 1 + 1 = 11 (carry 1)
   - **Example**: Adding binary numbers 11100 and 11010.

2. **Binary Subtraction**:
   - **Rules**:
     - 0 - 0 = 0
     - 1 - 0 = 1
     - 1 - 1 = 0
     - 10 - 1 = 1 (with borrowing from the next column if needed)
   - **Example**: Techniques vary, and different methods (like borrowing) can be used.

### Signed Binary Numbers

1. **Sign-Magnitude Representation**:
   - **Positive Numbers**: Sign bit is 0, the rest represent the magnitude.
   - **Negative Numbers**: Sign bit is 1, the rest represent the magnitude.
   - **Example**: +7 = 0000 0000 0000 0111 and -7 = 1000 0000 0000 0111 in 16-bit format.

### Two's Complement

1. **Definition**:
   - **1's Complement**: Invert all bits of the binary number.
   - **2's Complement**: 1's complement + 1.
   - **Example**: For 0110, 1's complement is 1001, and 2's complement is 1010.

2. **Important Properties**:
   - Taking the 2’s complement of a number twice returns the original number.
   - Provides a way to perform subtraction using addition.

### Data Storage in Memory

1. **Characters**:
   - Stored using ASCII or Unicode values.
   - **Example**: The word "cdac" in ASCII binary is 01100011 01100100 01100001 01100011.

2. **Integers**:
   - **Positive Integers**: Stored directly in binary format.
   - **Negative Integers**: Stored using 2’s complement representation.
   - **Example**: 
     - +65 = 00000000 00000000 00000000 01000001
     - -65 = 11111111 11111111 11111111 10111111 (using 2’s complement).

### Summary of Binary Representation

- **Positive 65**: `00000000 00000000 00000000 01000001`
- **Negative 65**: `11111111 11111111 11111111 10111111` (using 2's complement).


---

### **Positive and Negative Integers**

**1. Positive Integers**

- **Storage Format:** 4 bytes (32 bits)
  - **First Bit:** Sign bit (0 for positive)
  - **Remaining 31 Bits:** Value

**Example: Storing +65**

- **Decimal 65** in Binary: `00000000 00000000 00000000 01000001`
  
  **Memory Layout:**

  ```
  Byte 4  Byte 3  Byte 2  Byte 1
  00000000 00000000 00000000 01000001
  ```

**2. Negative Integers**

- **Storage Format:** 4 bytes (32 bits)
  - **First Bit:** Sign bit (1 for negative)
  - **Remaining 31 Bits:** 2’s complement of the absolute value

**Example: Storing -65**

- **Step 1: Convert 65 to Binary:**

  ```
  00000000 00000000 00000000 01000001
  ```

- **Step 2: Find 2’s Complement:**
  - **Invert Bits:** `11111111 11111111 11111111 10111110`
  - **Add 1:** `11111111 11111111 11111111 10111111`

  **Memory Layout:**

  ```
  Byte 4  Byte 3  Byte 2  Byte 1
  11111111 11111111 11111111 10111111
  ```

---

### **Floating Point Numbers**

**1. Conversion to Binary**

**Example: Decimal 4.25**

- **Integer Part:** `4` → Binary: `100`
- **Fractional Part:**
  - **0.25 * 2 = 0.50** (Take 0, next step: 0.50)
  - **0.50 * 2 = 1.00** (Take 1, stop)

  **Fractional Binary:** `.01`

- **Combined:** `4.25` in Binary: `100.01`

  **Normalized Form:** `1.01001 * 2^2`

**2. Normalization**

**Example: Decimal 10.75**

- **Binary Conversion:** `1010.11`
- **Normalized Form:** `1.01011 * 2^3`

  **Components:**
  - **Sign Bit:** `0` (positive)
  - **Exponent:**
    - **Actual Exponent:** `3`
    - **Bias for 8-bit Exponent:** `127`
    - **Stored Exponent:** `3 + 127 = 130` (Binary: `10000010`)
  - **Significant Value:** `01011` (after the decimal point)

  **Memory Layout:**

  ```
  Sign Bit | Exponent (8 bits) | Significant (23 bits)
  ------------------------------------------------------
  0        | 10000010           | 01011000000000000000000
  ```

---

### **Memory Storage and Classification**

**1. Memory Types**

| Type   | Description                                 | Example                 |
|--------|---------------------------------------------|-------------------------|
| **RAM**| Read/Write, Volatile                        | DRAM, SRAM               |
| **ROM**| Read-Only, Non-Volatile                     | PROM, EEPROM             |

**2. Memory Hierarchy**

| Level          | Speed       | Typical Capacity |
|----------------|-------------|------------------|
| **Registers**  | Fastest      | <1 KB            |
| **Cache**      | Fast         | 4 MB             |
| **Main Memory**| Moderate     | 1-8 GB           |
| **Magnetic Disk**| Slow       | 1-4 TB           |

---

### **RAM vs. ROM**

| Feature       | RAM                   | ROM                   |
|---------------|-----------------------|-----------------------|
| **Type**      | Volatile              | Non-Volatile          |
| **Read/Write**| Read/Write            | Read-Only             |
| **Usage**     | Store data, programs  | Booting, fixed data   |

---

### **Auxiliary Storage**

| Type            | Description                                  | Examples                      |
|-----------------|----------------------------------------------|-------------------------------|
| **HDD**         | Mechanical storage, high capacity, low cost | Hard Disk Drive                |
| **SSD**         | Electronic storage, faster, more durable    | Solid State Drive              |
| **Flash Memory**| Portable storage, non-volatile              | USB Flash Drive, SD Cards      |

**Diagram for Memory Layouts**

**1. Integer Storage:**

```
+-----------------------+
|    32-bit Integer      |
+-----------------------+
|  00000000 00000000    |
|  00000000 01000001    |  (+65)
+-----------------------+
```

**2. Floating Point Storage:**

```
+---------------------------+
|   32-bit Floating Point   |
+---------------------------+
|  Sign | Exponent | Signif. |
|  0    | 10000010 | 01011000|
+---------------------------+
```

**Diagram for Memory Hierarchy:**

```
Registers (Fastest)
    |
Cache
    |
Main Memory
    |
Magnetic Disk (Slowest)
```

---


### Detailed Notes on Memory Technologies and Concepts

#### Flash Memory

- **Definition**: Non-volatile memory that retains data even when there is no power supply.
- **Applications**: 
  - **Solid State Drives (SSD)**
  - **USB Drives**
  - **Memory Cards**
- **Characteristics**: 
  - **Low Power Consumption**
  - **Durable**
- **Varieties**:
  - **NAND Flash Memory**
  - **NOR Flash Memory**

##### Diagram of Flash Memory Types

```plaintext
+-----------------------+
|    Flash Memory       |
|-----------------------|
|   Non-Volatile        |
|   Retains Data        |
|   Low Power           |
|   Durable             |
|-----------------------|
|   NAND Flash Memory   |
|   NOR Flash Memory    |
+-----------------------+
```

#### Solid State Drive (SSD)

- **Definition**: Storage device that uses NAND flash memory.
- **Characteristics**:
  - **Faster** compared to traditional hard drives.
  - **More Durable** as there are no moving parts.

##### Diagram of SSD vs HDD

```plaintext
+-------------------+           +-------------------+
|      SSD          |           |      HDD          |
|-------------------|           |-------------------|
|   NAND Flash      |           |   Magnetic Disks  |
|   No Moving Parts |           |   Moving Parts    |
|   Faster Access   |           |   Slower Access   |
|   Durable         |           |   Less Durable    |
+-------------------+           +-------------------+
```

#### Optical Storage

- **Examples**: CD-ROM, DVD, Blu-ray Discs
- **Characteristics**:
  - **Magnetic Disks**: Contain information as pits or bumps on the disk.
  - **Usage**: Primarily for music, movies, etc.
- **Structure**:
  - **Single Spiral Track**: Runs from the center to the outer part of the disk.

##### Diagram of Optical Disk Structure

```plaintext
+----------------------+
|                      |
|  +----------+        |
|  |  Laser   |        |
|  +----------+        |
|       Spiral Track   |
|                      |
+----------------------+
```

#### Memory Interleaving

- **Definition**: Technique to improve memory access performance by distributing data across multiple memory modules or banks.
- **How it Works**:
  - **Round Robin Algorithm**: Data is distributed in a round-robin fashion.
  - **Parallel Access**: Allows for faster and more efficient access.
  - **Multi-core Processors**: Particularly beneficial for systems with multiple cores.

##### Diagram of Memory Interleaving Example

```plaintext
+----------------------+
| Memory Module 0      |
| Address: 0, 4, 8, ...|
+----------------------+
| Memory Module 1      |
| Address: 1, 5, 9, ...|
+----------------------+
| Memory Module 2      |
| Address: 2, 6, 10, ...|
+----------------------+
| Memory Module 3      |
| Address: 3, 7, 11, ...|
+----------------------+
```

#### Virtual Memory and Paging

- **Virtual Memory**: Allows a process to use more memory than physically available by using disk space.
- **Paging**: The process of dividing virtual memory into fixed-sized blocks called pages.
- **Page Table**: Maps virtual addresses to physical addresses.

##### Diagram of Virtual Memory and Paging

```plaintext
+------------------+
| Virtual Memory   |
|------------------|
| Page 0           |
| Page 1           |
| Page 2           |
| ...              |
+------------------+
        |
        v
+------------------+
| Physical Memory  |
|------------------|
| Frame 0          |
| Frame 1          |
| Frame 2          |
| ...              |
+------------------+
```

#### Page Replacement

- **Page Fault**: Occurs when a program accesses a page not currently in physical memory.
- **Replacement Policies**:
  - **Least Recently Used (LRU)**: Evicts the least recently used page.
  - **First In First Out (FIFO)**: Removes the oldest loaded page.
- **Thrashing**: Excessive page faults leading to performance degradation.
- **Demand Paging**: Pages are loaded only when required.
- **Dirty Bit**: Indicates if a page has been modified.

##### Table of Page Replacement Policies

| Policy            | Description                           | Example Usage   |
|-------------------|---------------------------------------|-----------------|
| **LRU**           | Evicts the least recently used page   | Cache systems   |
| **FIFO**          | Removes the oldest loaded page        | General use     |
| **Demand Paging** | Pages are loaded on demand             | Virtual Memory  |

#### Associative Memory

- **Definition**: Also known as Content-Addressable Memory (CAM). Retrieves data based on content rather than address.
- **Characteristics**:
  - **Parallel Search**: Allows for high-performance searches.
  - **Applications**: Cache memory, network routers, applications needing fast search.

##### Diagram of Associative Memory Operation

```plaintext
+--------------------+
| Data Storage       |
|--------------------|
| Keyword/Pattern    |
| Data               |
| ...                |
+--------------------+
        |
        v
+--------------------+
| Search Query       |
|--------------------|
| Compare with Data  |
| Retrieve Data      |
+--------------------+
```



### **1. Basics of Cache Memory**
- **Purpose**: To bridge the gap between the fast CPU and slower main memory.
- **Operation**: Frequently accessed data is stored in cache to reduce access times. The CPU first checks the cache before accessing main memory.

### **2. Principle of Locality**
- **Temporal Locality**: If data is accessed, it is likely to be accessed again soon.
- **Spatial Locality**: If data is accessed, data nearby is likely to be accessed soon.

### **3. Cache Performance Metrics**
- **Hit Ratio**: The percentage of cache accesses that are hits.
- **Miss Ratio**: The percentage of cache accesses that are misses.

### **4. Cache Lines and Blocks**
- **Cache Line**: A fixed-size block of memory transferred to and from the cache.
- **Example**: If the cache line size is 64 bytes and data at memory address 260 is requested, the entire block from bytes 256 to 319 is loaded into the cache.

### **5. Direct-Mapped Cache**
- **Mapping**: Memory addresses are divided into Tag, Index, and Offset.
- **Operation**: A single memory address maps to one specific cache line.
- **Example**: For a memory address, the Index determines which cache line to check, while the Tag ensures the correct data is retrieved.

### **6. Cache Coherence and Snooping**
- **Issue**: Ensuring all CPUs in a system have consistent views of memory.
- **Solution**: Cache snooping involves monitoring the bus to maintain coherence.
- **Write-Through**: Updates both the cache and main memory.
- **MESI Protocol**: Manages cache coherence with four states:
  - **Invalid**: Data is not valid.
  - **Shared**: Data is valid and possibly in other caches.
  - **Exclusive**: Data is valid and in only one cache.
  - **Modified**: Data is valid but not in other caches, and has been updated.

### **7. Multi-Level Cache**
- **Levels**: Typically, L1 (fastest), L2, and L3 (slowest, but still faster than main memory).
- **Purpose**: Reduces latency by having multiple cache levels with varying speeds and sizes.

### **8. Cache Optimization Techniques**
- **Cache Size**: Increasing cache size can improve performance but is costly.
- **Replacement Policies**: Include Least Recently Used (LRU), Most Recently Used (MRU), and Random.
- **Associativity**: How cache lines are mapped to cache slots (direct-mapped, associative, set-associative).
- **Prefetching**: Anticipating and loading data before it's requested.
- **Write Policies**: Write-back vs. Write-through.

### **9. UMA (Unified Memory Access) Symmetric Multiprocessor Architecture**
- **Simple Architecture**: All CPUs share a single bus.
- **Cache Addition**: Each CPU has its cache to reduce memory access conflicts.
- **Private and Shared Memory**: Each CPU has private cache and some shared memory.

### **10. Using Finite-State Machines (FSM) for Cache Control**
- **FSM Operation**: Manages cache operations, including read/write, cache coherence, and line replacement.
- **States**: Idle, Read, Write, Cache Miss, Cache Coherence.
- **Inputs**: External commands such as Read, Write requests.
- **Outputs**: Requests to main memory, cache updates, and notifications.



### Detailed Notes on CPU-I/O Device Communication and Parallel Computing

#### CPU-I/O Device Communication

**1. I/O-mapped I/O vs. Memory-mapped I/O**

| **Point**           | **I/O-mapped I/O**                   | **Memory-mapped I/O**          |
|----------------------|-------------------------------------|--------------------------------|
| **Address Space**    | Separate from memory                | Same as memory                  |
| **Instructions**     | Special instructions (IN, OUT)      | Same as memory instructions (LOAD/STORE/MOV) |
| **Compatibility**    | Older systems                       | Newer systems                   |

**2. Interrupt-Driven I/O (User Presses a Key)**

1. **Keyboard**: Generates an interrupt.
2. **CPU**: Stops its current task and runs the Interrupt Service Routine (ISR).
3. **ISR**: Communicates with the keyboard controller to read the keypress data (typically a scan code).
4. **CPU**: Stores the data in CPU registers or a memory buffer.
5. **CPU**: Resumes its previous tasks after handling the keypress.

**Diagram:**

```
[Keyboard] --> [Interrupt] --> [ISR] --> [Keyboard Controller] --> [Scan Code]
      |                                |
      |                                |
      v                                v
   [Data Stored in Register/Memory Buffer] --> [CPU Resumes Task]
```

**3. Direct Memory Access (DMA)**

1. **Keyboard**: Generates an interrupt.
2. **DMA Controller**: Reads keyboard data.
3. **DMA Controller**: Directly transfers data into a designated memory address.
4. **CPU**: Notified by the DMA controller when the transfer is complete.
5. **CPU**: Reads the keyboard data from memory and processes it.

**Diagram:**

```
[Keyboard] --> [Interrupt] --> [DMA Controller] --> [Memory Address]
                |                     |
                |                     v
                v               [CPU Notification]
        [Data Transfer]                |
                      ------------------
                                 |
                                 v
                             [CPU Reads Data]
```

#### Redundant Array of Independent Disks (RAID)

**1. Problem and Solution:**

- **Problem**: CPU performance has improved significantly, while disk performance has lagged.
- **Solution**: Use parallel I/O through RAID.

**2. RAID Techniques:**

- **Data Striping**: Distributes data across multiple drives for performance improvement.
- **Mirroring**: Duplicates data on multiple drives for redundancy.
- **Parity Techniques**: Provides redundancy without duplicating all data.

**3. RAID Levels:**

- **RAID 0**: Striping without redundancy; focuses on performance.
- **RAID 1**: Mirroring; provides data redundancy.
- **RAID 5**: Striping with distributed parity; balances performance and redundancy.
- **RAID 10 (1+0)**: Combines mirroring and striping; high performance and redundancy.
- **RAID 6**: Similar to RAID 5 but with dual parity for enhanced fault tolerance.

**4. RAID Techniques Detailed:**

- **Striping**: Breaks data into blocks and spreads them across multiple drives. Enhances performance but has no redundancy.

    **Diagram:**
    ```
    Data Block A1 | A2 | A3
    Disk 1    | B1 | B2 | B3
    Disk 2    | C1 | C2 | C3
    ```

- **Mirroring**: Copies the same data to two or more drives. Provides full redundancy but slower performance.

    **Diagram:**
    ```
    Disk 1: Block 1 | Block 2 | Block 3
    Disk 2: Block 1 | Block 2 | Block 3
    ```

- **Parity**: Stores parity information to reconstruct data in case of drive failure.

    **Diagram:**
    ```
    Disk A: Data 1
    Disk B: Data 2
    Disk C: Parity (D1 XOR D2)
    ```

#### CISC (Complex Instruction Set Computer) vs. RISC (Reduced Instruction Set Computer)

**1. CISC vs. RISC Architectures:**

- **CISC**:
  - Fetch -> Decode (and Interpret) -> Execute
  - More complex instructions, often requiring multiple clock cycles.
  - Less work for the programmer, more for the processor.

- **RISC**:
  - Fetch -> Decode -> Execute
  - Simpler instructions, typically one clock cycle per instruction.
  - More work for the programmer, less for the processor.

**2. Example Instructions:**

- **CISC**: `ADD A, B, C` (complex, multi-cycle)
- **RISC**: `LOAD X, A`, `LOAD Y, B`, `ADD Y, X`, `STORE Z` (simple, single-cycle)

**3. RISC Philosophy:**

- Direct execution by hardware.
- Maximize instruction issuance rate.
- Instructions should be easy to decode.
- Only LOAD and STORE should use memory.
- Provide a large number of registers.

#### ARM Architecture

- **Origins**: Developed by Acorn Computer in 1985, originally named Acorn RISC Machine, now known as ARM (Advanced RISC Machine).
- **Other RISC Architectures**: MIPS, PowerPC, RISC-V.

**Diagram:**

```
ARM Architecture Evolution
1980 - Berkeley VLSI RISC Design
1981 - Stanford MIPS
1985 - Acorn Archimedes (ARM)
```

#### Instruction-Level Parallelism: Pipelining

**1. Pipelining:**

- Break down Fetch-Decode-Execute into smaller stages.
- Use different hardware for each stage to improve throughput.

**Diagram:**

```
Stages: [Fetch] -> [Decode] -> [Execute]
         |       |         |
         v       v         v
         T1      T2        T3
```

**2. Superscalar Architecture:**

- Multiple pipelines in parallel (dual pipeline CPU).

**Diagram:**

```
Pipeline 1: [Fetch] -> [Decode] -> [Execute]
Pipeline 2: [Fetch] -> [Decode] -> [Execute]
```

#### On-Chip Parallelism

**1. Superscalar Processors:**

- Issue multiple instructions per cycle.
- Up to 2-6 instructions per cycle.

**2. VLIW (Very Long Instruction Word):**

- Compiler bundles instructions to be executed together.

**Diagram:**

```
Instruction Bundle: [L] [I] [F] [S]
L = Load, I = Integer, F = Float, S = Store
```

**3. On-Chip Multithreading:**

- **Fine-grained**: Switch threads in consecutive cycles.
- **Coarse-grained**: Switch threads only when the current one stalls.

**Diagram:**

```
Fine-Grained: A1 B1 C1 A2 B2 C2
Coarse-Grained: A1 A2 A3 B1 B2
```

**4. Single-Chip Multiprocessors:**

- Two or more CPUs on a single chip, sharing cache and memory.

**Diagram:**

```
CPU 1 [Core + Cache]
CPU 2 [Core + Cache]
```

#### Coprocessors

**1. Types of Coprocessors:**

- **Network Coprocessor**: Fast packet processing.
- **Graphics Processor (GPU)**: High-resolution graphics, SIMD operations.
- **Cryptoprocessor**: Encryption and decryption.

**Diagram:**

```
Coprocessor Types:
- Network Coprocessor
- Graphics Processor (GPU)
- Cryptoprocessor
```

#### Parallel Computers Terminology

**1. Instruction/Data Streams:**

| **Instruction Streams** | **Data Streams** | **Name**                  | **Examples**               |
|-------------------------|------------------|---------------------------|----------------------------|
| 1                       | 1                | SISD                      | Classical von Neumann machine |
| 1                       | Multiple         | SIMD                      | Vector supercomputer, Array processor |
| Multiple                | 1                | MISD                      | None                       |
| Multiple                | Multiple         | MIMD                      | Multiprocessor, Multicomputer |


### Multiprocessor Classifications

**Uniform Memory Access (UMA)**
- **Definition**: All CPUs have equal access time to every memory module.
- **Implication**: Simplifies memory access but may not scale efficiently for large systems.

**Non-Uniform Memory Access (NUMA)**
- **Definition**: Memory access time depends on the proximity to the CPU.
- **Implication**: More scalable for larger systems but requires careful management of memory locality.

### Message Passing

**Multicomputers (Distributed Memory)**
- **Technology**: Message Passing Interface (MPI)
- **Functions**:
  - `MPI_Send(buffer, count, data_type, destination, communicator)`
  - `MPI_Recv(&buffer, count, data_type, source, tag, communicator, &status)`
- **Focus**: Coarse-grained parallelism (process-level).

**Multiprocessors (Shared Memory)**
- **Technology**: OpenMP
- **Features**: Uses shared variables and directives for communication.
- **Focus**: Fine-grained parallelism (thread-level).

### Grid Computing

- **Definition**: Involves very large, international, loosely-coupled heterogeneous clusters.
- **Use Case**: Facilitates the sharing of resources across different organizations.

### NVLink

- **Definition**: High-speed, high-bandwidth interconnect technology developed by NVIDIA.
- **Benefits**: Faster communication between GPUs, CPUs, and other components compared to PCI Express; low latency and high bandwidth.

### Intel Processors

**32-bit vs. 64-bit Processors**
- **32-bit Processors**: Limited to 4GB RAM; struggles with memory-intensive applications.
- **64-bit Processors**: Supports up to 18.4 million TB of RAM; suitable for memory-intensive applications and backward compatible with 32-bit software.

**Generations of Intel Core Processors**
1. **First (Nehalem)** - 2008: Core i7, Core i5, Core i3
2. **Second (Sandy Bridge)** - 2011: Introduction of Intel Quick Sync Video
3. **Third (Ivy Bridge)** - 2012
4. **Fourth (Haswell)** - 2013
5. **Fifth (Broadwell)** - 2014
6. **Sixth (Skylake)** - 2015
7. **Seventh (Kaby Lake)** - 2016
8. **Eighth (Coffee Lake)** - 2017: More cores and threads
9. **Ninth (Coffee Lake Refresh)** - 2018
10. **Tenth (Comet Lake and Ice Lake)** - 2019
11. **Eleventh (Tiger Lake)** - 2020

### HPC Processors

**AMD**
- **Features**: High core counts, competitive performance, support for PCIe 4.0, and Infinity Fabric interconnect.
- **Notable Systems**: "Frontier" and "El Capitan" supercomputers.

**IBM POWER**
- **Features**: High core counts, significant memory bandwidth, advanced vector processing.
- **Notable Systems**: Summit supercomputer.

**ARM**
- **Features**: Power efficiency, scalability, heterogeneous computing.
- **Notable Systems**: "Fugaku" (world's fastest supercomputer) and "Astra" supercomputer.

