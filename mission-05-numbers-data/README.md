# Mission 5 — Numbers and data

## 1. Task / objective

Convert decimal, binary and hexadecimal numbers by hand, verify the answers using Python, build a number converter and explain how text is represented using encoding standards.

## 2. Work completed

### Task 5.1 — Convert numbers by hand

#### Decimal 13 to binary

| Division | Quotient | Remainder |
|---|---:|---:|
| 13 ÷ 2 | 6 | 1 |
| 6 ÷ 2 | 3 | 0 |
| 3 ÷ 2 | 1 | 1 |
| 1 ÷ 2 | 0 | 1 |

Reading the remainders from bottom to top gives `1101`.

Answer: **13 in decimal = 1101 in binary.**

#### Decimal 25 to binary

| Division | Quotient | Remainder |
|---|---:|---:|
| 25 ÷ 2 | 12 | 1 |
| 12 ÷ 2 | 6 | 0 |
| 6 ÷ 2 | 3 | 0 |
| 3 ÷ 2 | 1 | 1 |
| 1 ÷ 2 | 0 | 1 |

Reading the remainders from bottom to top gives `11001`.

Answer: **25 in decimal = 11001 in binary.**

#### Binary 1010 to decimal

Binary place values from right to left are 1, 2, 4 and 8.

`1 × 8 + 0 × 4 + 1 × 2 + 0 × 1 = 10`

Answer: **1010 in binary = 10 in decimal.**

#### Binary 1101 to decimal

`1 × 8 + 1 × 4 + 0 × 2 + 1 × 1 = 13`

Answer: **1101 in binary = 13 in decimal.**

#### Hexadecimal A to decimal

In hexadecimal, the digits after 9 are A, B, C, D, E and F, representing 10 through 15.

Answer: **A in hexadecimal = 10 in decimal.**

#### Hexadecimal 1F to decimal

`1 × 16 + 15 × 1 = 31`

Answer: **1F in hexadecimal = 31 in decimal.**

#### Binary 1111 to hexadecimal

`1 × 8 + 1 × 4 + 1 × 2 + 1 × 1 = 15`

Decimal 15 is hexadecimal F.

Answer: **1111 in binary = F in hexadecimal.**

### Task 5.2 — Verify using Python
| Expression tested | Python result | My observation |
|---|---|---|
| `bin(13)` | `'0b1101'` | The digits `1101` matched my manual conversion of 13. |
| `bin(25)` | `'0b11001'` | The digits `11001` matched the remainders I read from bottom to top. |
| `int("1010", 2)` | `10` | Python gave the same result as adding 8 and 2. |
| `int("1101", 2)` | `13` | Python gave the same result as adding 8, 4 and 1. |
| `int("A", 16)` | `10` | This confirmed that hexadecimal A represents decimal 10. |
| `int("1F", 16)` | `31` | The answer matched my calculation of 16 + 15. |
| `hex(15)` | `'0xf'` | Python used a lowercase `f` for hexadecimal F. |
| `hex(int("1111", 2))` | `'0xf'` | Binary `1111` and hexadecimal `F` represented the same value. |

The prefix `0b` identifies binary and `0x` identifies hexadecimal. Uppercase and lowercase hexadecimal letters represent the same values.

### Task 5.3 — Build a number converter

The program is saved in `number_converter.py`.

```python
number = int(input("Enter a positive decimal integer: "))

binary = bin(number)
hexadecimal = hex(number)

print("Binary:", binary)
print("Hexadecimal:", hexadecimal)
```

`input()` reads text entered by the user. `int()` converts that text to an integer. `bin()` and `hex()` return strings representing the integer in binary and hexadecimal. `print()` displays the results.

The program assumes a valid positive integer is supplied. It does not implement input validation.

Run from this mission folder:

```bash
python3 number_converter.py
```

| Input I entered | Binary output | Hexadecimal output |
|---:|---|---|
| 13 | `0b1101` | `0xd` |
| 25 | `0b11001` | `0x19` |
| 31 | `0b11111` | `0x1f` |

[I tested the program with three positive integers. For each input, it displayed one binary value and one hexadecimal value. For example, when I entered 31, the program displayed `0b11111` and `0x1f`. Both represent 31 in a different base.]
### Task 5.4 — How text is stored

The ASCII decimal code for uppercase `A` is **65**.

The ASCII decimal code for lowercase `a` is **97**.

A computer needs agreed encoding rules to represent characters using numbers and bytes. These rules allow software to store and interpret text consistently.

An example outside basic ASCII is the Bengali character **অ**.

ASCII defines a small set of characters. UTF-8 is an encoding for Unicode and supports a much wider range, including Bengali characters.

Python expressions for checking the two letter values:

```python
ord("A")
ord("a")
```

`ord()` returns a Unicode code point. For these characters, the values are the same as their ASCII codes.
[Python returned 65 for uppercase A and 97 for lowercase a. I could see that changing the case changes the character's numeric code.]
## 3. Commands / tools used

| Command / function | Purpose |
|---|---|
| `python3` | Start the Python interactive environment |
| `exit()` | Leave the interactive environment |
| `input()` | Read user input as text |
| `int()` | Convert text to an integer, optionally using a specified base |
| `bin()` | Return a binary representation |
| `hex()` | Return a hexadecimal representation |
| `print()` | Display output |
| `ord()` | Return a character's Unicode code point |
| `python3 number_converter.py` | Run the converter |

## 4. My understanding

Decimal uses base 10, binary uses base 2 and hexadecimal uses base 16.

Repeated division produces the digits of a number starting with the lowest place value, so the remainders must be read in reverse order.

Converting to decimal involves multiplying digits by their place values and adding the results.

A bit represents 0 or 1, and eight bits form a byte. Text encoding provides rules for representing characters using data.

## 5. Difficulties faced

[When I converted 13 to binary by hand, I got `1101`, but Python displayed `0b1101`. I was unsure whether my answer matched.]

## 6. How I resolved them

[I learned that `0b` marks a binary number and `0x` marks a hexadecimal number. The digits after `0b` were `1101`, so Python’s result matched my calculation.]

## 7. Evidence / files

- `README.md`.
- `number_converter.py`.
- Manual conversion working.
- Interactive verification results.
- Three actual converter test results.

## 8. Commit details

Planned commit message: `Build number converter and practise data representation`

Commit, push and GitHub verification: [Not verified]