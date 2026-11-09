# Classes de equivalência (avançado)

Particionamento em classes válidas e inválidas para os campos *State*, *Last Name*, *User ID* e *Student ID*. Conteúdo original em inglês.

### State

the standard Post Office two-character abbreviation for the states, districts, territories, etc. of the United States.

| \# | Equivalence class | Test input example | Expected result |
|:--:|:--:|:--:|:--:|
| 1 | Positive Class - Two-letter state abbreviation | NY | Accepted |
| 2 | Negative Class - More than two characters | CAL | Rejected |
| 3 | Negative Class - Less than two characters | N | Rejected |
| 4 | Negative Class - Non-alphabetic characters | N1 | Rejected |
| 5 | Negative Class - One Lowercase lettter | Ny | Rejected |
| 6 | Negative Class - Special Character | N\* | Rejected |
| 7 | Negative Class - One Space | 'N ’ | Rejected |

### Last Name

one to fifteen characters, can contain alphabetic characters, periods, hyphens, apostrophes, spaces, and numbers.

| \# | Equivalence class | Test input example | Expected result |
|:--:|:--:|:--:|:--:|
| 1 | Positive Class - Alphabetic name | Daniel | Accepted |
| 2 | Negative Class - Includes hyphen or apostrophe | Daniel’s | Accepted |
| 3 | Negative Class - Includes spaces | Daniel Silva | Accepted |
| 4 | Negative Class - Includes numbers | Daniel1 | Accepted |
| 5 | Negative Class - More than 15 characters | DanielSilvaNogueira | Rejected |
| 6 | Negative Class - input empty | ‘’ | Rejected |

### User ID

eight characters at least two of which are not alphabetic (numeric, special, nonprinting).

| \# | Equivalence class | Test input example | Expected result |
|:--:|:--:|:--:|:--:|
| 1 | Positive Class - 8 characters, at least 2 non-alphabetic | user123!@ | Accepted |
| 2 | Negative Class - Less than 8 characters | user123 | Rejected |
| 3 | Negative Class - Only alphabetic characters | username | Rejected |
| 4 | Negative Class - Only numeric characters | 12345678 | Rejected |
| 5 | Negative Class - Only special characters | !@#\$%ˆ&\* | Rejected |
| 6 | Negative Class - Only one non alphabetical | abcdef1 | Rejected |
| 7 | Positive Class - more than 8 characters | abcdefg@1 | Accepted |

### Student ID

eight characters. The first two represent the student's home campus while the last six are a unique six-digit number. Valid home campus abbreviations are:

1.  AN, Annandale;

2.  LC, Las Cruces;

3.  RW, Riverside West;

4.  SM, San Mateo;

5.  TA, Talbot;

6.  WE, Weber;

7.  WN, Wenatchee.

| \# | Equivalence class | Test input example | Expected result |
|:--:|:--:|:--:|:--:|
| 1 | Positive Class - Starts with a correct campus code and has 6 digits | AN123456 | Accepted |
| 2 | Negative Class - Starts with an incorrect campus code | 08123456 | Rejected |
| 3 | Negative Class - Less than 8 characters | AN12345 | Rejected |
| 4 | Negative Class - More than 8 characters | 081234567 | Rejected |
| 5 | Negative Class - Last 6 characters are not all numbers | 08USERID | Rejected |
