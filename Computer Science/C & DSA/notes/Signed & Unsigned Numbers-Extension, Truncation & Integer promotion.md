
# 2A. Signed and Unsigned Numbers in Memory

## Default Behavior

In C, `int` is **signed by default**.

```c
int y = -9;
```

A signed integer stores `-9` using **2's complement representation**.

For a 32-bit integer:

```text
-9 = 11111111 11111111 11111111 11110111
```

This bit pattern is fixed in memory.

---

## Printing the Same Bit Pattern Differently

### Example

```c
int y = -9;

printf("%d", y);
printf("%u", y);
```

### Output

```text
-9
4294967287
```

### Why?

The bit pattern remains the same:

```text
11111111 11111111 11111111 11110111
```

- `%d` → Treats the bit pattern as a **signed integer**
- `%u` → Treats the same bit pattern as an **unsigned integer**

Therefore:

```text
%d → -9
%u → Huge positive number
```

> The memory representation does not change. Only the interpretation changes.

---

## Unsigned Integer Example

```c
unsigned int y = -9;

printf("%d", y);
printf("%u", y);
```

### Output

```text
-9           (implementation-dependent behavior due to format mismatch)
4294967287
```

The stored bits are still:

```text
11111111 11111111 11111111 11110111
```

When interpreted as unsigned:

```text
4294967287
```

---

# Extension and Truncation

---

## Extension

### Definition

Extension means converting a smaller datatype into a larger datatype.

Example:

```text
short → int
char → int
```

---

## Types of Extension

### 1. Sign Extension

Used when the source datatype is **signed**.

The MSB (Most Significant Bit) is copied into the newly created bits.

---

### Example 1

```c
short int x = 9;
int ix = x;
```

`x` (16 bits)

```text
0000 0000 0000 1001
```

`ix` (32 bits)

```text
0000 0000 0000 0000 0000 0000 0000 1001
```

Extra bits are filled with `0`.

---

### Example 2

```c
short int y = -9;
int iy = y;
```

16-bit representation of `-9`:

```text
1111 1111 1111 0111
```

After sign extension:

```text
1111 1111 1111 1111 1111 1111 1111 0111
```

The new bits are filled with `1` because the sign bit is `1`.

---

### Rule

For signed source variables:

```text
MSB = 0 → fill new bits with 0
MSB = 1 → fill new bits with 1
```

This process is called **Sign Extension**.

---

## 2. Zero Extension

Used when the source datatype is **unsigned**.

New bits are always filled with `0`.

---

### Example

```c
unsigned short int y = -9;
unsigned int iy = y;
```

`y` (16 bits)

```text
1111 1111 1111 0111
```

After zero extension:

```text
0000 0000 0000 0000 1111 1111 1111 0111
```

The newly created higher bits are all zeros.

---

## Important Rule

Extension depends on the **source (RHS) datatype**, not the destination datatype.

```c
short int y = -9;
unsigned int iy = y;
```

Since the source (`y`) is signed:

```text
Sign extension occurs first
```

Result:

```text
11111111 11111111 11111111 11110111
```

Even though the destination is unsigned.

---

### Summary

| Source Type | Extension Used |
|------------|---------------|
| Signed | Sign Extension |
| Unsigned | Zero Extension |

---

# Truncation

---

## Definition

Truncation occurs when a larger datatype is assigned to a smaller datatype.

Example:

```c
int → short
int → char
```

The higher-order bits are discarded.

---

## Important Rule

Truncation happens first regardless of whether the source or destination is signed/unsigned.

---

### Example

```c
int x = -9;
short y = x;
```

32-bit representation:

```text
11111111 11111111 11111111 11110111
```

After truncating to 16 bits:

```text
11111111 11110111
```

Only the lower 16 bits are copied.

---

### Observation

Truncation can drastically change:

- Value
- Sign
- Meaning of the number

because high-order bits are lost.

---

## Rule

```text
Extension → Copy new bits
Truncation → Discard higher bits
```

---

# Integer Promotion

---

## Definition

Before many arithmetic operations and function calls, smaller integer types are automatically converted to `int`.

This is called **Integer Promotion**.

Examples:

```c
char
short
unsigned char
unsigned short
```

are usually promoted to:

```c
int
```

(or `unsigned int` in some cases)

---

## Example

```c
unsigned short int y = -9;

int iy = y;

printf("%d", y);
printf("%u", y);

printf("%d", iy);
printf("%u", iy);
```

### Step 1: Store `-9` in unsigned short

16-bit representation:

```text
11111111 11110111
```

Value:

```text
65527
```

---

### Step 2: Integer Promotion

When passed to `printf()`:

```c
printf("%d", y);
printf("%u", y);
```

`y` is first promoted to `int`.

Since `y` is an unsigned short, promotion preserves the value:

```text
65527
```

Thus:

```text
%d → 65527
%u → 65527
```

---

## Another Example

```c
short int y = -9;
unsigned int iy = y;
```

### Sign Extension

```text
11111111 11111111 11111111 11110111
```

Stored in `iy`.

---

### Printing

```c
printf("%d", iy);
```

Interprets the bit pattern as signed:

```text
-9
```

```c
printf("%u", iy);
```

Interprets the same bit pattern as unsigned:

```text
4294967287
```

---

# Key Takeaways

## Signed vs Unsigned

- Memory stores only bits.
- Signedness affects interpretation, not storage.

---

## Extension

- Small type → Large type
- Depends on source type.
- Signed → Sign Extension
- Unsigned → Zero Extension

---

## Truncation

- Large type → Small type
- Higher bits are discarded.
- Can completely change value/sign.

---

## Integer Promotion

- `char` and `short` are usually promoted to `int`.
- Happens automatically in:
  - Arithmetic operations
  - Function arguments (`printf`, etc.)
  - Expressions

---

## Golden Rules

```text
Extension depends on RHS/source type.

Signed source   → Sign Extension
Unsigned source → Zero Extension

Truncation always removes higher bits.

Memory stores bits;
%d and %u simply interpret them differently.
```