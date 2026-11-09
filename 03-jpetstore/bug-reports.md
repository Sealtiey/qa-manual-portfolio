# JPetStore — Bug reports

Bug reports completos (pré-condições, passos, resultado esperado/atual, ambiente, severidade e prioridade) escritos durante os testes do JPetStore. Os anexos apontam para as evidências (prints/vídeos) enviadas na época. Conteúdo original em inglês.

> Os IDs recomeçam em cada tarefa (cada arquivo era uma entrega separada).

## Sign-in page

### PS-001 — The 'Password' field is filled with 4 characters on the 'Sign in' page by default after opening

| Field | Value |
|---|---|
| Preconditions | User is not logged in |
| Steps to reproduce | 1. Go to link<br>2. Click 'Sign In' link<br>3. Pay attention to the 'Password' field<br>https://petstore.octoperf.com/actions/Catalog.action |
| Actual result | The 'Password' field is filled with 4 characters by default. |
| Expected result | The 'Password' field is empty by default |
| Attachments | [Screenshot: https://imgur.com/4xd0Mzs](https://imgur.com/4xd0Mzs)<br>Video: https://www.loom.com/share/6d08a2008f914ce3930582466628e76f<br>https://www.loom.com/share/6d08a2008f914ce3930582466628e76f |
| Notes | The reason is the html attribute ‘value’ that contains the value ‘j2ee’ |
| Operating system | MacOS 15 (Sequoia) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Moderate |
| Priority | Medium |

## Help page

### PS-001 — Clicking on the 'Known Issues' link does not redirect the user to the 'Known Issues' section on the Help page

| Field | Value |
|---|---|
| Preconditions | User has access to the website. |
| Steps to reproduce | 1. Open the website.<br>2. Click on the ”?” icon.<br>3. Click on the “Known Issues” link. |
| Actual result | The page does not scroll down to the “Known Issues” section. |
| Expected result | This issue may be related to a missing link |
| Attachments | Screenshot (Google Drive — link removido) |
| Operating system | MacOS 14 (Sonoma) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Moderate |
| Priority | Medium |

## Registration page

### PS-001 — Selecting Japanese as the language preference does not change the website language; it remains in English.

| Field | Value |
|---|---|
| Preconditions | The user has access to the website. |
| Steps to reproduce | 1. Open the website.<br>2. Click on Sign In.<br>3. Click on Register Now.<br>4. Click on the Language Preference dropdown.<br>5. Select Japanese. |
| Actual result | The website remains in English even after selecting Japanese. |
| Expected result | The website should switch to Japanese after selecting it as the preferred language. |
| Attachments | [screenrec](https://screenrec.com/share/tpSwzC3yfX) |
| Operating system | MacOS 14 (Sonoma) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Moderate |
| Priority | Medium |

### PS-002 — Entering an invalid email format (e.g., @@@) in the email field does not trigger an error message; instead, the page simply reloads.

| Field | Value |
|---|---|
| Preconditions | The user has access to the website. |
| Steps to reproduce | 1. Open the website.<br>2. Click on Sign In.<br>3. Click on Register Now.<br>4. Fill in the email field with an invalid value (e.g., @@@).<br>5. Click on Save Account Information. |
| Actual result | The page reloads without displaying an error message. |
| Expected result | The system should display a validation error indicating that the email format is incorrect. |
| Attachments | Screenshot:<br>[screenrec](https://screenrec.com/share/WKqkCnEHXv) |
| Operating system | MacOS 14 (Sonoma) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Major |
| Priority | High |

### PS-003 — The fields filled in on the Register Now page persist even after closing and reopening the website.

| Field | Value |
|---|---|
| Preconditions | The user has accessed the Register Now page and filled in some fields. |
| Steps to reproduce | 1. Open the website.<br>2. Click Log In.<br>3. Click Register Now.<br>4. Fill in any of the fields (e.g. email, phone, city).<br>5. Close the browser or refresh the page.<br>6. Reopen the website and navigate back to Register Now. |
| Actual result | The previously entered values remain in the form fields. |
| Expected result | The fields should be cleared when the session ends or the page is reloaded. |
| Attachments | Screenshot:<br>[screenrec](https://screenrec.com/share/svaIt69BGN) |
| Operating system | MacOS 14 (Sonoma) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Moderate |
| Priority | Medium |
