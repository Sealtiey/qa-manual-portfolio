# Conduit — Test Cases (export do TestRail)

Suite **Master** do projeto Conduit no TestRail, exportada em XML e convertida para Markdown. A estrutura de seções segue a decomposição do site (usuário deslogado / logado → página → componente). Os casos foram escritos em inglês, como no original.

**Total de casos:** 120  
**Por prioridade:** High: 73, Medium: 37, Low: 7, Critical: 3

## Estrutura de seções

- User disconnected
  - Home page
    - Feed global
      - Article Preview
        - "User Profile” Link
        - [Like] Button
        - Article Information  (Title and Description)
        - Tags
    - Popular Tags
      - Tag
  - Sign In page
    - "Sign In" Form
      - "Email" Field (7 casos)
      - "Password" Field (9 casos)
      - [Sign In] Button (2 casos)
    - "Need an Account? Link" (2 casos)
  - Sign Up page
    - "Sign Up" Form (2 casos)
      - "Username" Field (6 casos)
      - "Email" Field (6 casos)
      - "Password" Field (7 casos)
      - [Sign Up] Button (2 casos)
    - "Have an Account? Link" (1 caso)
  - Article page
    - Article header (6 casos)
      - "User profile" link (3 casos)
      - Post data (3 casos)
      - [Follow: username] button (4 casos)
      - [Favorite article] button (Favorite article) (4 casos)
    - Article text (2 casos)
    - Tags (2 casos)
    - Comments
      - Comment text (2 casos)
      - User profile link (1 caso)
      - Post data (1 caso)
  - User page
    - User Banner
      - User Icon
      - User Name
      - [Follow: username:]
    - My publications
      - Article view
    - Favorite publications
      - Article view
- User logged in
  - Home page (3 casos)
    - Feed Navigation (5 casos)
      - “Your Feed” Tab
        - Article Preview (2 casos)
        - “User Profile” Link (1 caso)
        - [Like] Button (3 casos)
        - Article Information (Title and Description) (1 caso)
        - Tags (2 casos)
    - “Global Feed” Tab
      - Article Preview
      - "User Profile” Link
      - [Like] Button
      - Article Information  (Title and Description)
      - Tags
    - Popular Tags
      - Tag List
  - New Article page
    - “Article Title” Field (3 casos)
    - "What’s this article about?” Field (2 casos)
    - “Write your article (in markdown)” Field (2 casos)
    - “Enter Tags” Field (2 casos)
    - [Publish Article] Button (2 casos)
  - Settings
    - "Your Settings" Form
      - “URL of profile picture” Field (3 casos)
      - "Username” Field (2 casos)
      - “Short bio about you” Field (3 casos)
      - “Email” Field (3 casos)
      - “New Password” Field (6 casos)
      - [Update Settings] Button (green) (2 casos)
    - [Or click here to logout] Button (red) (1 caso)
  - User page
    - User Banner
      - User Icon
      - User Name
      - [Edit Profile Settings]
    - My posts
      - Empty State Message (Text: “No articles are here… yet.”)
    - Favorited Posts
      - Empty State Message (Text: “No articles are here… yet.”)
  - Article page
    - Article header
      - Article title
      - "User profile" link
      - Post data
      - [Edit Article] button
      - [Delete Article] button
    - Article text
    - Tags
    - Comments
      - "Write a comment…” Field
      - [Post Comment] button

## Casos de teste

### User disconnected › Sign In page › "Sign In" Form › "Email" Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C28 | Positive - Enter valid email and valid password | Critical | Other |
| C29 | Positive - Enter valid username and valid password | Critical | Other |
| C30 | Negative - Submit with empty “Email” field | High | Other |
| C31 | Negative - Submit with unregistered email | High | Other |
| C32 | Negative - Submit with unregistered username | High | Other |
| C33 | Positive - Email field displays correct placeholder text | Low | Other |
| C45 | Negative - Send with empty "Email" field displays a validation message. Approximate message: "Email: cannot be blank" | High | Other |

### User disconnected › Sign In page › "Sign In" Form › "Password" Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C34 | Negative - Submit with empty password field | High | Other |
| C35 | Positive - Password input is covered with asterisks | Medium | Other |
| C36 | Positive - Attempt to copy password (should not work) | Medium | Other |
| C37 | Positive - Attempt to cut password (should not work) | Medium | Other |
| C38 | Positive - Paste value into password field (should work) | Medium | Other |
| C39 | Negative - Submit with valid username/email and invalid password | High | Other |
| C40 | Negative - Submit with both fields empty | High | Other |
| C46 | Negative - Sending with empty password field shows validation message. Approximate message: “Password: cannot be blank” | High | Other |
| C49 | Positive - Clicking on the ‘Send a one-time password’ link redirects to the Forgot password page | Medium | Other |

### User disconnected › Sign In page › "Sign In" Form › [Sign In] Button

| ID | Title | Priority | Type |
|---|---|---|---|
| C41 | Positive - Click on Sign In button to submit valid credentials | Critical | Other |
| C42 | Positive - Press Enter key to submit valid credentials | High | Other |

### User disconnected › Sign In page › "Need an Account? Link"

| ID | Title | Priority | Type |
|---|---|---|---|
| C43 | Positive - “Need an account?” link is visible on Sign In page | Medium | Other |
| C44 | Positive - Click on “Need an account?” redirects to Sign Up page | Medium | Other |

### User disconnected › Sign Up page › "Sign Up" Form

| ID | Title | Priority | Type |
|---|---|---|---|
| C1 | Login with valid credentials | High | Other |
| C27 | Positive - Register a new user with valid credentials | High | Other |

### User disconnected › Sign Up page › "Sign Up" Form › "Username" Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C9 | Negative - Attempt to register with a username that is already taken | High | Other |
| C11 | Negative - Attempt to register with a username shorter than 3 characters | High | Other |
| C12 | Negative - Attempt to register with a username longer than 40 characters | Medium | Other |
| C13 | Negative - Attempt to register with a username containing invalid special characters | High | Other |
| C14 | Negative - Attempt to register with a username that does not start with a letter | High | Other |
| C15 | Negative - Attempt to register with a username containing spaces or non-printable characters | High | Other |

### User disconnected › Sign Up page › "Sign Up" Form › "Email" Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C6 | Positive - Register a new user and verify the verification email is sent | High | Other |
| C3 | Login with mandatory field blank | Medium | Other |
| C10 | Negative - Attempt to register with an email that is already taken | High | Other |
| C16 | Negative - Attempt to register with an invalid email format (missing @ or invalid domain) | High | Other |
| C17 | Negative - Attempt to register with an email containing unsupported special characters | Medium | Other |
| C18 | Negative - Attempt to register without filling in the email field | High | Other |

### User disconnected › Sign Up page › "Sign Up" Form › "Password" Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C2 | Login with incorrect password | High | Other |
| C20 | Negative - Attempt to register with a password shorter than 8 characters | High | Other |
| C21 | Negative - Attempt to register with a password longer than 30 characters | Medium | Other |
| C22 | Negative - Attempt to register with a password missing special characters | High | Other |
| C23 | Negative - Attempt to register with a password missing uppercase letters | High | Other |
| C24 | Negative - Attempt to register with a password missing numbers | High | Other |
| C19 | Negative - Attempt to register without filling in the password field | High | Other |

### User disconnected › Sign Up page › "Sign Up" Form › [Sign Up] Button

| ID | Title | Priority | Type |
|---|---|---|---|
| C5 | Positive - Register a new user and verify navigation to the “Finish Registration” page | Medium | Other |
| C7 | Positive - Register a user by pressing Enter instead of clicking the “Sign Up” button | Medium | Other |

### User disconnected › Sign Up page › "Have an Account? Link"

| ID | Title | Priority | Type |
|---|---|---|---|
| C8 | Positive - Navigate to the login page by clicking the “Have an account?” link | Medium | Other |

### User disconnected › Article page › Article header

| ID | Title | Priority | Type |
|---|---|---|---|
| C50 | Positive - Clicking on “User profile” link redirects to author’s profile | High | Other |
| C51 | Positive - Post data (author name and publication date) is displayed correctly | Medium | Other |
| C52 | Positive - [Follow: username] button appears for other authors and toggles correctly | High | Other |
| C53 | Negative - [Follow] button appears for user’s own article | Low | Other |
| C54 | Positive - [Favorite article] button toggles article favorite status | High | Other |
| C55 | Negative - [Favorite article] button does not update count when clicked | Medium | Other |

### User disconnected › Article page › Article header › "User profile" link

| ID | Title | Priority | Type |
|---|---|---|---|
| C64 | Positive – User is redirected to author’s profile after clicking the username | High | Other |
| C65 | Negative – Incorrect user profile is opened after clicking username | High | Other |
| C66 | Negative – User clicks the profile link but nothing happens | Medium | Other |

### User disconnected › Article page › Article header › Post data

| ID | Title | Priority | Type |
|---|---|---|---|
| C67 | Positive – Article displays correct username and post date | Medium | Other |
| C68 | Negative – Post date is not displayed | Low | Other |
| C69 | Negative – Username displayed is different from the actual article author | High | Other |

### User disconnected › Article page › Article header › [Follow: username] button

| ID | Title | Priority | Type |
|---|---|---|---|
| C70 | Positive – User can follow another author by clicking [Follow: username] | High | Other |
| C71 | Positive – Button changes to [Unfollow] after being clicked | Medium | Other |
| C72 | Negative – Follow button appears when viewing own article | Low | Other |
| C73 | Negative – Follow button does not persist state after page reload | Medium | Other |

### User disconnected › Article page › Article header › [Favorite article] button (Favorite article)

| ID | Title | Priority | Type |
|---|---|---|---|
| C74 | Positive – Clicking [Favorite] adds article to favorites and increases count | High | Other |
| C75 | Positive – Clicking again removes from favorites and count decreases | Medium | Other |
| C76 | Negative – Favorite count does not update after interaction | Medium | Other |
| C77 | Negative – Unauthenticated user clicks Favorite and is not redirected to Sign In | High | Other |

### User disconnected › Article page › Article text

| ID | Title | Priority | Type |
|---|---|---|---|
| C56 | Positive - Full article text is displayed correctly | High | Other |
| C57 | Negative - Article body text cuts off or displays improperly | Medium | Other |

### User disconnected › Article page › Tags

| ID | Title | Priority | Type |
|---|---|---|---|
| C58 | Positive - Tags are displayed below the article text | Medium | Other |
| C59 | Negative - Tags with invalid characters are rendered incorrectly | Low | Other |

### User disconnected › Article page › Comments › Comment text

| ID | Title | Priority | Type |
|---|---|---|---|
| C60 | Positive - New comments are displayed under the article | High | Other |
| C61 | Negative - Comment text allows more than allowed character limit | Medium | Other |

### User disconnected › Article page › Comments › User profile link

| ID | Title | Priority | Type |
|---|---|---|---|
| C62 | Positive - Clicking on commenter’s username redirects to their profile | Medium | Other |

### User disconnected › Article page › Comments › Post data

| ID | Title | Priority | Type |
|---|---|---|---|
| C63 | Positive - Comment date and author are displayed correctly | Medium | Other |

### User logged in › Home page

| ID | Title | Priority | Type |
|---|---|---|---|
| C109 | Access Home page by clicking the “Conduit” logo | High | Other |
| C110 | Access Home page by clicking the “Conduit” logo | High | Other |
| C111 | Verify banner text and background color on the Home page | Low | Other |

### User logged in › Home page › Feed Navigation

| ID | Title | Priority | Type |
|---|---|---|---|
| C112 | Verify that “Your Feed” tab is visible only for logged-in users | High | Other |
| C113 | Verify that “Your Feed” tab shows followed users’ articles | High | Other |
| C114 | Verify that “Global Feed” tab shows all articles sorted from newest to oldest | High | Other |
| C115 | Check that pagination is displayed below the articles | Medium | Other |
| C116 | Check that only 10 articles are displayed per page | High | Other |

### User logged in › Home page › Feed Navigation › “Your Feed” Tab › Article Preview

| ID | Title | Priority | Type |
|---|---|---|---|
| C117 | Verify each article preview contains author avatar, username, date, title, description, and “Read more…” link | High | Other |
| C118 | Verify the date is shown in DD.MM.YYYY format | Medium | Other |

### User logged in › Home page › Feed Navigation › “Your Feed” Tab › “User Profile” Link

| ID | Title | Priority | Type |
|---|---|---|---|
| C119 | Clicking the author username redirects to the user profile page | High | Other |

### User logged in › Home page › Feed Navigation › “Your Feed” Tab › [Like] Button

| ID | Title | Priority | Type |
|---|---|---|---|
| C120 | Like button is visible only for logged-in users | High | Other |
| C121 | Clicking Like button increases like count | High | Other |
| C122 | Clicking Like again removes the like (unlike) | High | Other |

### User logged in › Home page › Feed Navigation › “Your Feed” Tab › Article Information (Title and Description)

| ID | Title | Priority | Type |
|---|---|---|---|
| C123 | Clicking article title, description or “Read more…” redirects to Article page | High | Other |

### User logged in › Home page › Feed Navigation › “Your Feed” Tab › Tags

| ID | Title | Priority | Type |
|---|---|---|---|
| C124 | Popular Tags” section is displayed to the right of the feed | Medium | Other |
| C125 | Clicking a tag filters the articles containing that tag | High | Other |

### User logged in › New Article page › “Article Title” Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C78 | Positive – Filling with valid title (5-240 characters) | High | Other |
| C79 | Negative – Empty field shows error: “Title of the article can’t be empty (minimum 5 symbols)” | High | Other |
| C80 | Warning – Non-unique title shows warning: “Article with a similar Title already exists. Do you want to continue?” | Medium | Other |

### User logged in › New Article page › "What’s this article about?” Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C81 | Positive – Filling with valid short description (5-240 characters) | High | Other |
| C82 | Negative – Empty field shows error: “Description of the article can’t be empty (minimum 5 symbols)” | High | Other |

### User logged in › New Article page › “Write your article (in markdown)” Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C83 | Positive – Article body with 20+ characters is accepted | High | Other |
| C84 | Negative – Empty field shows error: “Body of article can’t be blank.” | High | Other |

### User logged in › New Article page › “Enter Tags” Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C85 | Positive – Valid tag starting with “#” is accepted | Medium | Other |
| C86 | Negative – Invalid tag (missing “#” or containing special characters) is rejected | Medium | Other |

### User logged in › New Article page › [Publish Article] Button

| ID | Title | Priority | Type |
|---|---|---|---|
| C87 | Positive – Publishes article with valid data and redirects to the Article page | High | Other |
| C88 | Negative – Attempt to publish with empty required fields shows validation messages | High | Other |

### User logged in › Settings › "Your Settings" Form › “URL of profile picture” Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C89 | Enter a valid image URL in the profile picture field | High | Other |
| C90 | Submit a non-URL string in the profile picture field | High | Other |
| C91 | Leave the profile picture field empty and update settings | Low | Other |

### User logged in › Settings › "Your Settings" Form › "Username” Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C92 | Update the username with a valid new one | High | Other |
| C93 | Leave username field blank and try to update | High | Other |

### User logged in › Settings › "Your Settings" Form › “Short bio about you” Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C94 | Add a valid short bio with letters, numbers, and special characters | Medium | Other |
| C95 | Add a bio with more than 9000 characters | Medium | Other |
| C96 | Add a bio starting or ending with multiple spaces | Medium | Other |

### User logged in › Settings › "Your Settings" Form › “Email” Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C97 | Update the email with a valid new one | High | Other |
| C98 | Try logging in with the old email after updating | High | Other |
| C99 | Try logging in with the new email after updating | High | Other |

### User logged in › Settings › "Your Settings" Form › “New Password” Field

| ID | Title | Priority | Type |
|---|---|---|---|
| C100 | Update the password with a valid strong one | High | Other |
| C101 | Try to reuse the same current password | High | Other |
| C102 | Try a password with less than 8 or more than 30 characters | High | Other |
| C103 | Check if the new password is masked (hidden) | Medium | Other |
| C104 | Try logging in with the old password after updating | High | Other |
| C105 | Try logging in with the new password after updating | High | Other |

### User logged in › Settings › "Your Settings" Form › [Update Settings] Button (green)

| ID | Title | Priority | Type |
|---|---|---|---|
| C106 | Update settings with valid values in all mandatory fields | High | Other |
| C107 | Try to update settings with invalid or empty required fields | High | Other |

### User logged in › Settings › [Or click here to logout] Button (red)

| ID | Title | Priority | Type |
|---|---|---|---|
| C108 | Click on the logout button and check if user is redirected to Home and logged out | High | Other |
