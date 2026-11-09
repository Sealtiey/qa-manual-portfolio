# Mockup testing — app mobile de terapia

Análise de um mockup de app mobile (telas de login, lista de terapeutas e perfil): 3 bugs encontrados, cada um com um caso de teste correspondente. Títulos dos bugs em português e casos em inglês, como no original.

### Bug 1: Erro de digitação em “Forgot password?”

**Test Case 1**

- **Title:** Verify “Forgot password?” text

- **Precondition:** User is on the Log in screen.

- **Steps:**

  1.  Open the Log in screen.

  2.  Locate the “Forgot password?” link.

- **Expected result:** The text should be displayed as **“Forgot password?”**

- **Actual result:** The text is displayed as **“Forgot pasword?”**

- **Severity:** Minor

### Bug 2: Erro de digitação em “Therapists”

**Test Case 2**

- **Title:** Verify Therapists page title

- **Precondition:** User is on the Therapists screen.

- **Steps:**

  1.  Open the Therapists screen.

  2.  Check the page title.

- **Expected result:** The title should be displayed as **“Therapists”**.

- **Actual result:** The title is displayed as **“Therapits”**.

- **Severity:** Minor

### Bug 3: Erro de digitação em “Reviews”

**Test Case 3**

- **Title:** Verify reviews tab label

- **Precondition:** User is on a therapist profile.

- **Steps:**

  1.  Open a therapist profile.

  2.  Check the tabs displayed below the therapist information.

  3.  Locate the reviews tab.

- **Expected result:** The tab should be labeled **“REVIEWS”**.

- **Actual result:** The tab is labeled **“RECENSIONS”**.

- **Severity:** Minor
