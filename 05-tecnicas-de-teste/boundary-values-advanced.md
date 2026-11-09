# Valores-limite (avançado)

Valores-limite para os campos *ZIP Code*, *Last Name*, *User ID* e *Course ID*. Conteúdo original em inglês.

### ZIP Code

Must contain 5 digits. The minimum value is 01000. The maximum value is 99999.
| \# | Boundary value | Test input example | Expected result |
|:--:|:--:|:--:|:--:|
| 1 | Lower boundary (5 digits, min valid) | 01000 | Accepted |
| 2 | Just below lower boundary (4 digits) | 999 | Rejected |
| 3 | Upper boundary (5 digits, max valid) | 99999 | Accepted |
| 4 | Just above upper boundary (6 digits) | 100000 | Rejected |

### Last Name

one to fifteen characters, can contain alphabetic characters, periods, hyphens, apostrophes, spaces, and numbers.
| \# | Boundary value | Test input example | Expected result |
|:--:|:--:|:--:|:--:|
| 1 | Lower boundary (1 character, min valid) | A | Accepted |
| 2 | Just below lower boundary (empty string) | “” | Rejected |
| 3 | Upper boundary (15 characters, max valid) | A.-'b abced1234 | Accepted |
| 4 | Just above upper boundary (16 characters) | ABCDEFGHIJKLMNOP | Rejected |

### User ID

eight characters at least two of which are not alphabetic (numeric, special, nonprinting).

| \# | Boundary value | Test input example | Expected result |
|:--:|:--:|:--:|:--:|
| 1 | Lower boundary (8 characters, min valid) | Ab1@5678 | Accepted |
| 2 | Just below lower boundary (7 characters) | A1b2C3! | Rejected |
| 3 | Invalid - Above the upper limit (9 characters) | A1b2C3!#2 | Rejected |
| 4 | Invalid - Only alphabetic characters | abcdefgh | Rejected |
| 5 | Invalid - Only numeric characters | 12345678 | Rejected |
| 6 | Invalid - Only special characters | !@#\$%^&\* | Rejected |
| 7 | Valid - At least two non-alphabetical characters | abcdefg1 | Accepted |

### Course ID

three alpha characters representing the department followed by a six-digit integer which is the unique course identification number. The possible departments are:

1.  PHY - Physics

2.  EGR - Engineering

3.  ENG - English

4.  LAN - Foreign languages

5.  CHM - Chemistry

6.  MAT - Mathematics

7.  PED - Physical education

8.  SOC - Sociology

| \# | Boundary value | Test input example | Expected result |
|:--:|:--:|:--:|:--:|
| 1 | Lower boundary (3 letters + 6 digits, min valid) | PHY000000 | Accepted |
| 2 | Just below lower boundary (2 letters + 6 digits) | PH999999 | Rejected |
| 3 | Upper boundary (3 letters + 6 digits, max valid) | PHY999999 | Accepted |
| 4 | Just above upper boundary (4 letters + 6 digits) | PHYS999999 | Rejected |
| 5 | Invalid - Non-numeric last 6 characters | PHYABCDEF | Rejected |
