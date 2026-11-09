# Conduit — Test Runs (export do TestRail)

Execuções registradas no TestRail para o Conduit, exportadas em XML e convertidas para Markdown. Bugs encontrados foram reportados no Jira (projeto `CON`) e vinculados ao resultado do teste no campo *Defects*.

## Resumo

| Test Run | Data | Testes | Passed | Failed | Blocked | Retest | Untested |
|---|---|---|---|---|---|---|---|
| [My first Test Run 01/04/2025](#my-first-test-run-01042025) | 2025-04-01 | 3 | 3 | 0 | 0 | 0 | 0 |
| [Sign Up Test Run 05/04/2025](#sign-up-test-run-05042025) | 2025-04-05 | 24 | 15 | 9 | 0 | 0 | 0 |
| [Sign In Test Run 08/04/2025](#sign-in-test-run-08042025) | 2025-04-08 | 20 | 17 | 3 | 0 | 0 | 0 |
| [New Article Test Run 14/04/2025](#new-article-test-run-14042025) | 2025-04-14 | 10 | 0 | 0 | 0 | 0 | 10 |
| [Regression Test Execution 14/04/2025](#regression-test-execution-14042025) | 2025-04-14 | 18 | 0 | 0 | 0 | 0 | 18 |
| [Running a home page test 14/04/2025](#running-a-home-page-test-14042025) | 2025-04-14 | 17 | 0 | 0 | 0 | 0 | 17 |
| [Running configuration tests 14/04/2025](#running-configuration-tests-14042025) | 2025-04-14 | 20 | 0 | 0 | 0 | 0 | 20 |
| [Smoke test execution 14/04/2025](#smoke-test-execution-14042025) | 2025-04-14 | 10 | 0 | 0 | 0 | 0 | 10 |

Total: 8 test runs, 122 execuções de casos (35 passed, 12 failed, 0 blocked).

## My first Test Run 01/04/2025

Criado em 2025-04-01 · arquivo original: `my_first_test_run_01_04_2025.xml`

| Test | Case | Section | Title | Priority | Status | Defects | Comment |
|---|---|---|---|---|---|---|---|
| T1 | C1 | Sign Up page › "Sign Up" Form | Login with valid credentials | High | Passed |  |  |
| T3 | C3 | "Sign Up" Form › "Email" Field | Login with mandatory field blank | Medium | Passed |  | password: can't be blank  email: can't be blank |
| T2 | C2 | "Sign Up" Form › "Password" Field | Login with incorrect password | High | Passed |  | email or password: is invalid |

## Sign Up Test Run 05/04/2025

Criado em 2025-04-05 · arquivo original: `sign_up_test_run_05_04_2025.xml`

| Test | Case | Section | Title | Priority | Status | Defects | Comment |
|---|---|---|---|---|---|---|---|
| T4 | C1 | Sign Up page › "Sign Up" Form | Login with valid credentials | High | Passed |  |  |
| T29 | C27 | Sign Up page › "Sign Up" Form | Positive - Register a new user with valid credentials | High | Passed |  |  |
| T11 | C9 | "Sign Up" Form › "Username" Field | Negative - Attempt to register with a username that is already taken | High | Passed |  |  |
| T13 | C11 | "Sign Up" Form › "Username" Field | Negative - Attempt to register with a username shorter than 3 characters | High | Failed | CON-5 |  |
| T14 | C12 | "Sign Up" Form › "Username" Field | Negative - Attempt to register with a username longer than 40 characters | Medium | Failed | CON-9 |  |
| T15 | C13 | "Sign Up" Form › "Username" Field | Negative - Attempt to register with a username containing invalid special characters | High | Passed |  |  |
| T16 | C14 | "Sign Up" Form › "Username" Field | Negative - Attempt to register with a username that does not start with a letter | High | Passed |  |  |
| T17 | C15 | "Sign Up" Form › "Username" Field | Negative - Attempt to register with a username containing spaces or non-printable characters | High | Passed |  |  |
| T8 | C6 | "Sign Up" Form › "Email" Field | Positive - Register a new user and verify the verification email is sent | High | Failed | CON-10 |  |
| T6 | C3 | "Sign Up" Form › "Email" Field | Login with mandatory field blank | Medium | Passed |  |  |
| T12 | C10 | "Sign Up" Form › "Email" Field | Negative - Attempt to register with an email that is already taken | High | Passed |  |  |
| T18 | C16 | "Sign Up" Form › "Email" Field | Negative - Attempt to register with an invalid email format (missing @ or invalid domain) | High | Passed |  |  |
| T19 | C17 | "Sign Up" Form › "Email" Field | Negative - Attempt to register with an email containing unsupported special characters | Medium | Failed | CON-11 |  |
| T20 | C18 | "Sign Up" Form › "Email" Field | Negative - Attempt to register without filling in the email field | High | Passed |  |  |
| T5 | C2 | "Sign Up" Form › "Password" Field | Login with incorrect password | High | Passed |  |  |
| T22 | C20 | "Sign Up" Form › "Password" Field | Negative - Attempt to register with a password shorter than 8 characters | High | Failed | CON-12 |  |
| T23 | C21 | "Sign Up" Form › "Password" Field | Negative - Attempt to register with a password longer than 30 characters | Medium | Failed | CON-13 |  |
| T24 | C22 | "Sign Up" Form › "Password" Field | Negative - Attempt to register with a password missing special characters | High | Failed | CON-14 |  |
| T25 | C23 | "Sign Up" Form › "Password" Field | Negative - Attempt to register with a password missing uppercase letters | High | Failed | CON-15 |  |
| T26 | C24 | "Sign Up" Form › "Password" Field | Negative - Attempt to register with a password missing numbers | High | Failed | CON-16 |  |
| T21 | C19 | "Sign Up" Form › "Password" Field | Negative - Attempt to register without filling in the password field | High | Passed |  |  |
| T7 | C5 | "Sign Up" Form › [Sign Up] Button | Positive - Register a new user and verify navigation to the “Finish Registration” page | Medium | Passed |  |  |
| T9 | C7 | "Sign Up" Form › [Sign Up] Button | Positive - Register a user by pressing Enter instead of clicking the “Sign Up” button | Medium | Passed |  |  |
| T10 | C8 | Sign Up page › "Have an Account? Link" | Positive - Navigate to the login page by clicking the “Have an account?” link | Medium | Passed |  |  |

## Sign In Test Run 08/04/2025

Criado em 2025-04-08 · arquivo original: `sign_in_test_run_08_04_2025.xml`

| Test | Case | Section | Title | Priority | Status | Defects | Comment |
|---|---|---|---|---|---|---|---|
| T30 | C28 | "Sign In" Form › "Email" Field | Positive - Enter valid email and valid password | Critical | Passed |  |  |
| T31 | C29 | "Sign In" Form › "Email" Field | Positive - Enter valid username and valid password | Critical | Failed | CON-20 |  |
| T32 | C30 | "Sign In" Form › "Email" Field | Negative - Submit with empty “Email” field | High | Passed |  |  |
| T33 | C31 | "Sign In" Form › "Email" Field | Negative - Submit with unregistered email | High | Passed |  |  |
| T34 | C32 | "Sign In" Form › "Email" Field | Negative - Submit with unregistered username | High | Failed | CON-22 |  |
| T35 | C33 | "Sign In" Form › "Email" Field | Positive - Email field displays correct placeholder text | Low | Passed |  |  |
| T36 | C45 | "Sign In" Form › "Email" Field | Negative - Send with empty "Email" field displays a validation message. Approximate message: "Email: cannot be blank" | High | Passed |  |  |
| T39 | C34 | "Sign In" Form › "Password" Field | Negative - Submit with empty password field | High | Passed |  |  |
| T40 | C35 | "Sign In" Form › "Password" Field | Positive - Password input is covered with asterisks | Medium | Passed |  |  |
| T41 | C36 | "Sign In" Form › "Password" Field | Positive - Attempt to copy password (should not work) | Medium | Passed |  |  |
| T42 | C37 | "Sign In" Form › "Password" Field | Positive - Attempt to cut password (should not work) | Medium | Passed |  |  |
| T43 | C38 | "Sign In" Form › "Password" Field | Positive - Paste value into password field (should work) | Medium | Passed |  |  |
| T44 | C39 | "Sign In" Form › "Password" Field | Negative - Submit with valid username/email and invalid password | High | Passed |  |  |
| T45 | C40 | "Sign In" Form › "Password" Field | Negative - Submit with both fields empty | High | Passed |  |  |
| T46 | C46 | "Sign In" Form › "Password" Field | Negative - Sending with empty password field shows validation message. Approximate message: “Password: cannot be blank” | High | Passed |  |  |
| T47 | C49 | "Sign In" Form › "Password" Field | Positive - Clicking on the ‘Send a one-time password’ link redirects to the Forgot password page | Medium | Failed | CON-21 | Test is blocked because the “Forgot password” page is not implemented yet. |
| T48 | C41 | "Sign In" Form › [Sign In] Button | Positive - Click on Sign In button to submit valid credentials | Critical | Passed |  |  |
| T49 | C42 | "Sign In" Form › [Sign In] Button | Positive - Press Enter key to submit valid credentials | High | Passed |  |  |
| T50 | C43 | Sign In page › "Need an Account? Link" | Positive - “Need an account?” link is visible on Sign In page | Medium | Passed |  |  |
| T51 | C44 | Sign In page › "Need an Account? Link" | Positive - Click on “Need an account?” redirects to Sign Up page | Medium | Passed |  |  |

## New Article Test Run 14/04/2025

Criado em 2025-04-14 · arquivo original: `new_article_test_run_14_04_2025.xml`

| Test | Case | Section | Title | Priority | Status | Defects | Comment |
|---|---|---|---|---|---|---|---|
| T190 | C78 | New Article page › “Article Title” Field | Positive – Filling with valid title (5-240 characters) | High | Untested |  |  |
| T191 | C79 | New Article page › “Article Title” Field | Negative – Empty field shows error: “Title of the article can’t be empty (minimum 5 symbols)” | High | Untested |  |  |
| T192 | C81 | New Article page › "What’s this article about?” Field | Positive – Filling with valid short description (5-240 characters) | High | Untested |  |  |
| T193 | C82 | New Article page › "What’s this article about?” Field | Negative – Empty field shows error: “Description of the article can’t be empty (minimum 5 symbols)” | High | Untested |  |  |
| T194 | C83 | New Article page › “Write your article (in markdown)” Field | Positive – Article body with 20+ characters is accepted | High | Untested |  |  |
| T195 | C84 | New Article page › “Write your article (in markdown)” Field | Negative – Empty field shows error: “Body of article can’t be blank.” | High | Untested |  |  |
| T196 | C85 | New Article page › “Enter Tags” Field | Positive – Valid tag starting with “#” is accepted | Medium | Untested |  |  |
| T197 | C86 | New Article page › “Enter Tags” Field | Negative – Invalid tag (missing “#” or containing special characters) is rejected | Medium | Untested |  |  |
| T198 | C87 | New Article page › [Publish Article] Button | Positive – Publishes article with valid data and redirects to the Article page | High | Untested |  |  |
| T199 | C88 | New Article page › [Publish Article] Button | Negative – Attempt to publish with empty required fields shows validation messages | High | Untested |  |  |

## Regression Test Execution 14/04/2025

Criado em 2025-04-14 · arquivo original: `regression_test_execution_14_04_2025.xml`

| Test | Case | Section | Title | Priority | Status | Defects | Comment |
|---|---|---|---|---|---|---|---|
| T175 | C28 | "Sign In" Form › "Email" Field | Positive - Enter valid email and valid password | Critical | Untested |  |  |
| T176 | C30 | "Sign In" Form › "Email" Field | Negative - Submit with empty “Email” field | High | Untested |  |  |
| T177 | C39 | "Sign In" Form › "Password" Field | Negative - Submit with valid username/email and invalid password | High | Untested |  |  |
| T178 | C40 | "Sign In" Form › "Password" Field | Negative - Submit with both fields empty | High | Untested |  |  |
| T179 | C46 | "Sign In" Form › "Password" Field | Negative - Sending with empty password field shows validation message. Approximate message: “Password: cannot be blank” | High | Untested |  |  |
| T172 | C9 | "Sign Up" Form › "Username" Field | Negative - Attempt to register with a username that is already taken | High | Untested |  |  |
| T173 | C16 | "Sign Up" Form › "Email" Field | Negative - Attempt to register with an invalid email format (missing @ or invalid domain) | High | Untested |  |  |
| T174 | C20 | "Sign Up" Form › "Password" Field | Negative - Attempt to register with a password shorter than 8 characters | High | Untested |  |  |
| T187 | C112 | Home page › Feed Navigation | Verify that “Your Feed” tab is visible only for logged-in users | High | Untested |  |  |
| T188 | C114 | Home page › Feed Navigation | Verify that “Global Feed” tab shows all articles sorted from newest to oldest | High | Untested |  |  |
| T189 | C115 | Home page › Feed Navigation | Check that pagination is displayed below the articles | Medium | Untested |  |  |
| T180 | C78 | New Article page › “Article Title” Field | Positive – Filling with valid title (5-240 characters) | High | Untested |  |  |
| T181 | C83 | New Article page › “Write your article (in markdown)” Field | Positive – Article body with 20+ characters is accepted | High | Untested |  |  |
| T182 | C87 | New Article page › [Publish Article] Button | Positive – Publishes article with valid data and redirects to the Article page | High | Untested |  |  |
| T183 | C88 | New Article page › [Publish Article] Button | Negative – Attempt to publish with empty required fields shows validation messages | High | Untested |  |  |
| T184 | C100 | "Your Settings" Form › “New Password” Field | Update the password with a valid strong one | High | Untested |  |  |
| T185 | C104 | "Your Settings" Form › “New Password” Field | Try logging in with the old password after updating | High | Untested |  |  |
| T186 | C106 | "Your Settings" Form › [Update Settings] Button (green) | Update settings with valid values in all mandatory fields | High | Untested |  |  |

## Running a home page test 14/04/2025

Criado em 2025-04-14 · arquivo original: `running_a_home_page_test_14_04_2025.xml`

| Test | Case | Section | Title | Priority | Status | Defects | Comment |
|---|---|---|---|---|---|---|---|
| T200 | C109 | User logged in › Home page | Access Home page by clicking the “Conduit” logo | High | Untested |  |  |
| T201 | C110 | User logged in › Home page | Access Home page by clicking the “Conduit” logo | High | Untested |  |  |
| T202 | C111 | User logged in › Home page | Verify banner text and background color on the Home page | Low | Untested |  |  |
| T203 | C112 | Home page › Feed Navigation | Verify that “Your Feed” tab is visible only for logged-in users | High | Untested |  |  |
| T204 | C113 | Home page › Feed Navigation | Verify that “Your Feed” tab shows followed users’ articles | High | Untested |  |  |
| T205 | C114 | Home page › Feed Navigation | Verify that “Global Feed” tab shows all articles sorted from newest to oldest | High | Untested |  |  |
| T206 | C115 | Home page › Feed Navigation | Check that pagination is displayed below the articles | Medium | Untested |  |  |
| T207 | C116 | Home page › Feed Navigation | Check that only 10 articles are displayed per page | High | Untested |  |  |
| T208 | C117 | “Your Feed” Tab › Article Preview | Verify each article preview contains author avatar, username, date, title, description, and “Read more…” link | High | Untested |  |  |
| T209 | C118 | “Your Feed” Tab › Article Preview | Verify the date is shown in DD.MM.YYYY format | Medium | Untested |  |  |
| T210 | C119 | “Your Feed” Tab › “User Profile” Link | Clicking the author username redirects to the user profile page | High | Untested |  |  |
| T211 | C120 | “Your Feed” Tab › [Like] Button | Like button is visible only for logged-in users | High | Untested |  |  |
| T212 | C121 | “Your Feed” Tab › [Like] Button | Clicking Like button increases like count | High | Untested |  |  |
| T213 | C122 | “Your Feed” Tab › [Like] Button | Clicking Like again removes the like (unlike) | High | Untested |  |  |
| T214 | C123 | “Your Feed” Tab › Article Information (Title and Description) | Clicking article title, description or “Read more…” redirects to Article page | High | Untested |  |  |
| T215 | C124 | “Your Feed” Tab › Tags | Popular Tags” section is displayed to the right of the feed | Medium | Untested |  |  |
| T216 | C125 | “Your Feed” Tab › Tags | Clicking a tag filters the articles containing that tag | High | Untested |  |  |

## Running configuration tests 14/04/2025

Criado em 2025-04-14 · arquivo original: `running_configuration_tests_14_04_2025.xml`

| Test | Case | Section | Title | Priority | Status | Defects | Comment |
|---|---|---|---|---|---|---|---|
| T217 | C89 | "Your Settings" Form › “URL of profile picture” Field | Enter a valid image URL in the profile picture field | High | Untested |  |  |
| T218 | C90 | "Your Settings" Form › “URL of profile picture” Field | Submit a non-URL string in the profile picture field | High | Untested |  |  |
| T219 | C91 | "Your Settings" Form › “URL of profile picture” Field | Leave the profile picture field empty and update settings | Low | Untested |  |  |
| T220 | C92 | "Your Settings" Form › "Username” Field | Update the username with a valid new one | High | Untested |  |  |
| T221 | C93 | "Your Settings" Form › "Username” Field | Leave username field blank and try to update | High | Untested |  |  |
| T222 | C94 | "Your Settings" Form › “Short bio about you” Field | Add a valid short bio with letters, numbers, and special characters | Medium | Untested |  |  |
| T223 | C95 | "Your Settings" Form › “Short bio about you” Field | Add a bio with more than 9000 characters | Medium | Untested |  |  |
| T224 | C96 | "Your Settings" Form › “Short bio about you” Field | Add a bio starting or ending with multiple spaces | Medium | Untested |  |  |
| T225 | C97 | "Your Settings" Form › “Email” Field | Update the email with a valid new one | High | Untested |  |  |
| T226 | C98 | "Your Settings" Form › “Email” Field | Try logging in with the old email after updating | High | Untested |  |  |
| T227 | C99 | "Your Settings" Form › “Email” Field | Try logging in with the new email after updating | High | Untested |  |  |
| T228 | C100 | "Your Settings" Form › “New Password” Field | Update the password with a valid strong one | High | Untested |  |  |
| T229 | C101 | "Your Settings" Form › “New Password” Field | Try to reuse the same current password | High | Untested |  |  |
| T230 | C102 | "Your Settings" Form › “New Password” Field | Try a password with less than 8 or more than 30 characters | High | Untested |  |  |
| T231 | C103 | "Your Settings" Form › “New Password” Field | Check if the new password is masked (hidden) | Medium | Untested |  |  |
| T232 | C104 | "Your Settings" Form › “New Password” Field | Try logging in with the old password after updating | High | Untested |  |  |
| T233 | C105 | "Your Settings" Form › “New Password” Field | Try logging in with the new password after updating | High | Untested |  |  |
| T234 | C106 | "Your Settings" Form › [Update Settings] Button (green) | Update settings with valid values in all mandatory fields | High | Untested |  |  |
| T235 | C107 | "Your Settings" Form › [Update Settings] Button (green) | Try to update settings with invalid or empty required fields | High | Untested |  |  |
| T236 | C108 | Settings › [Or click here to logout] Button (red) | Click on the logout button and check if user is redirected to Home and logged out | High | Untested |  |  |

## Smoke test execution 14/04/2025

Criado em 2025-04-14 · arquivo original: `smoke_test_execution_14_04_2025.xml`

| Test | Case | Section | Title | Priority | Status | Defects | Comment |
|---|---|---|---|---|---|---|---|
| T76 | C28 | "Sign In" Form › "Email" Field | Positive - Enter valid email and valid password | Critical | Untested |  |  |
| T87 | C39 | "Sign In" Form › "Password" Field | Negative - Submit with valid username/email and invalid password | High | Untested |  |  |
| T88 | C40 | "Sign In" Form › "Password" Field | Negative - Submit with both fields empty | High | Untested |  |  |
| T89 | C41 | "Sign In" Form › [Sign In] Button | Positive - Click on Sign In button to submit valid credentials | Critical | Untested |  |  |
| T75 | C27 | Sign Up page › "Sign Up" Form | Positive - Register a new user with valid credentials | High | Untested |  |  |
| T55 | C5 | "Sign Up" Form › [Sign Up] Button | Positive - Register a new user and verify navigation to the “Finish Registration” page | Medium | Untested |  |  |
| T158 | C112 | Home page › Feed Navigation | Verify that “Your Feed” tab is visible only for logged-in users | High | Untested |  |  |
| T160 | C114 | Home page › Feed Navigation | Verify that “Global Feed” tab shows all articles sorted from newest to oldest | High | Untested |  |  |
| T133 | C87 | New Article page › [Publish Article] Button | Positive – Publishes article with valid data and redirects to the Article page | High | Untested |  |  |
| T154 | C108 | Settings › [Or click here to logout] Button (red) | Click on the logout button and check if user is redirected to Home and logged out | High | Untested |  |  |
