# JPetStore — Bug summaries

Resumos curtos de bugs (o quê / onde / quando + evidência), primeiro formato de reporte praticado antes do bug report completo. Conteúdo original em inglês.

## Bug summary

| ID | What happened? | Where? | When? | Evidence |
|---|---|---|---|---|
| PS 0001 | A product that is out of stock can still be added to the shopping cart, proceed to checkout, and be purchased | Shopping cart screen | After adding an out-of-stock product and proceeding to checkout. | [screenshot](https://ibb.co/8gMyfzZJ) |
| PS 0002 | On the ”?” page, when clicked, it redirects to a page where there is no back button, causing a navigation break. | On the ”?” icon | When clicking on the ”?” icon. | [screenshot](https://ibb.co/tpX8F5pG) |
| PS 0003 | The Total Cost does not update automatically when changing the product quantity. The value only updates after clicking “Update Cart”. | Shopping cart screen | After changing the product quantity in the shopping cart. | [screenshot](https://ibb.co/DgK9MX22) |
| PS 0004 | HTTP Error when proceding with registration<br>*Note:* Instead of an HTTP Status 500 error, the system should display a validation message informing the user about the missing required fields. | Register Now screen | After the user tries to register without filling in the other required fields. | [screenrec](https://screenrec.com/share/ByZOw8VEda) |
| PS 0005 | On the “Register Now” page, when all fields are correctly filled in, clicking “Save Account” reloads the page and redirects to the “Main Menu” instead of logging in automatically. | Register Now screen | After the user tries to register, the login does not happen automatically. | [screenshot](https://ibb.co/jk5078SX) |

## Primeiro bug summary

| ID | What happened? | Where? | When? | Evidence |
|---|---|---|---|---|
| PS-001 | The user is not redirected to the 'Known Issues' paragraph | On the Help page | After cliking on the 'Known Issues' link | [Loom video](https://www.loom.com/share/596fc0222164489a999d2f0ed2ef378d?sid=60a2ed14-fb7b-4cbc-ba26-25a3a7caa9aa) |
