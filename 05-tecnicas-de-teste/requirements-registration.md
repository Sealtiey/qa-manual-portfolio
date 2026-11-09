# Refinamento de requisitos — Registro

Reescrita dos requisitos da página de registro para que fiquem atômicos, consistentes, sem ambiguidade, completos e testáveis. Conteúdo original em inglês.

## Registration

“The ‘Registration’ page allows users to register by filling in required fields. After clicking the registration button, they gain access to product ordering.”

Users should be able to open the “Sign Up” page from the “Sign In” page by clicking on the “Register Now!” button.

The “Registration” form should contain two blocks: “User Information” and “Account Information”.

Users should be able to create an account by clicking on the \[Save Account Information\] button or pressing an Enter button.

“If there is no conflict with the credentials, the user is registered and logged in automatically.”

## User Information

The “User Information” section should contain 3 required fields: User ID, New Password, and Repeat Password. All required fields should be marked by asterisks.

## Username

Required field and should be unique, also should contain up to 40 symbols;

Should accept Latin letters and digits;

Special characters and non-printing symbols are not allowed;

No case-sensitive.

## New Password

Optional field;

User shouldn’t be able to copy/cut/paste from this field;

Should be covered by a mask;

Min 8 symbols, max 30 symbols;

Non-printing symbols are not allowed;

New Password: must contain at least one uppercase letter, one lowercase letter, one digit, and one special character (*allowed characters: !@#\$%^&*()*\_+-={}\[\]\|:;\<\>,.?/~*) Spaces are not allowed.”

## Confirm password

Required field;

User shouldn’t be able to copy/cut from this field;

Should contain 8-32 symbols;

The value should match with the Password field.

## Account Information

The “Account information” section contains the information about a user. It could be filled optionally during the registration process or after.

## Email

The format of email is \[name\]@\[domain\].com;

Should contain 14 - 72 symbols;

\[name\] part accepts Latin letters, digits, and some special characters: plus (+), hyphen (-), underline (\_), dot (.);

Should be unique;

Required field.

## Phone

Should have a placeholder: *+38 098 765 43 21;*

The number should start from the plus;

Letters, special characters, and non-printing symbols are not allowed.

## Profile Information

This section contains optional additional information about preferences about the user account.

Language available options: EN, ES, UK, Japanese.

In the Favorite Category, Users should be able to select a single favorite category for discount emails.

The Enable My Banner checkbox is a required checkbox checked by default. If the user checks this selection checkbox, the additional useful info banner in the footer should be shown.

## Validation

For the registration with an already registered User ID, the informative validation message should be shown.

If some of the required fields are not filled, these fields should be marked in red.

If validation fails, an error message should specify which fields contain errors. Example: ‘Validation failed! Please check the Email and Password fields.’”.
