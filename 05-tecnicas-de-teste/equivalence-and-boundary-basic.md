# Classes de equivalência e valores-limite — campo de senha

Exercício básico: classes de equivalência e valores-limite para um campo de senha de 4 a 16 caracteres que exige letra maiúscula e caractere especial. Conteúdo original em inglês.

### Part I: Equivalence classes

| \# | Equivalence class | Test input example | Expected result |
|:--:|:--:|:--:|:--:|
| 1 | Negative Class (3 characters) | Abc | Input Rejected |
| 2 | Positive Class (4 characters, one uppercase letter, one special character) | Abc@1 | Input Accepted |
| 3 | Negative Class (17 characters, one uppercase letter, one special character) | Abcdefghijkmn@123 | Input Rejected |
| 4 | Negative Class (8 characters, NO uppercase letter, one special character) | abcde@123 | Input Rejected |
| 5 | Negative Class (8 characters, missing special character) | Abcde123 | Input Rejected |

### Part II: Boundary values

| \# | Boundary value | Test input example | Expected result |
|:--:|:--:|:--:|:--:|
| 1 | First class, boundary (3 characters) | Ab1 | Input Rejected |
| 2 | Second class, boundary (4 characters) | Abc1 | Input Accepted |
| 3 | First class, boundary (16 characters) | Abcdefghi@123456 | Input Accepted |
| 4 | Second class, boundary (17 characters) | Abcdefghi@1234567" | Input Rejected |
