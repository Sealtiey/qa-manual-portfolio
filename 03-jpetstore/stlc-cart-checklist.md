# JPetStore — STLC: checklist do carrinho, execução e report

Ciclo completo de teste (STLC) sobre os requisitos do **carrinho** do JPetStore: desenho de um checklist, execução, registro de bugs e relatório de execução. Conteúdo original em inglês.

## Test execution statistics (run de 26/03/2025)

| Total tests | Executed | Execution rate | Passed | Pass rate | Failed |
|---|---|---|---|---|---|
| 34 | 33 | 97.06% | 25 | 75.76% | 8 |

## Bug statistics by severity

| Severity | Bugs | % |
|---|---|---|
| Critical | 0 | 0% |
| Major | 6 | 85.71% |
| Moderate | 1 | 14.29% |
| Minor | 0 | 0% |
| **Total** | **7** | |

## Checklist — Cart

| # | Checklist item | Priority | Result | Bug ID | Comment |
|---|---|---|---|---|---|
| 1 | Ensure that the user can access the cart from any page in the application. | Critical | Passed |  |  |
| 2 | Ensure that the cart icon displays the tooltip “Carrinho” | Medium | Failed | PS-001 |  |
| 3 | The cart should have a column “Item ID” | Critical | Passed |  |  |
| 4 | The cart should have a column “Product ID” | Critical | Passed |  |  |
| 5 | The cart should have a column “Name” | Critical | Failed | PS-002 |  |
| 6 | The cart should have a column “Description” | Critical | Passed |  |  |
| 7 | The cart should have a column “In Stock?" | Critical | Passed |  |  |
| 8 | The cart should have a column “Quantity” | Critical | Passed |  |  |
| 9 | The cart should have a column “List Price” | Critical | Passed |  |  |
| 10 | The cart should have a column “Total Cost. | Critical | Passed |  |  |
| 11 | Ensure that the last row of the product table contains the subtotal | Critical | Passed |  |  |
| 12 | Ensure that the last row of the product table contains an “Update Cart” button. | Critical | Passed |  |  |
| 13 | Ensure that the cart is empty by default and displays the message “Your cart is empty”. | High | Passed |  |  |
| 14 | Ensure that the “Proceed to checkout” button appears if at least one product is in the cart. | Critical | Passed |  |  |
| 15 | Ensure that clicking “Proceed to checkout” redirects logged-in users to the checkout page. | Critical | Passed |  |  |
| 16 | Ensure that clicking “Proceed to Checkout” redirects non-logged-in users to the login page. | Critical | Passed |  |  |
| 17 | Ensure that users can exit the cart page by clicking the “Return to Main Menu” link. | High | Passed |  |  |
| 18 | Ensure that the “Add to Cart” button is available on the Product Detail Page (PDP) | Critical | Passed |  |  |
| 19 | Ensure that the “Add to Cart” button is available on the product listing. | Critical | Passed |  |  |
| 20 | Ensure that adding a product to the cart updates the cart icon with a badge showing the total quantity. | High | Failed | PS-003 |  |
| 21 | Ensure that the “Item ID” fields in the cart contain clickable links to the product. | Medium | Passed |  |  |
| 22 | Ensure that the “Name” fields in the cart contain clickable links to the product. | Medium | Skipped |  |  |
| 23 | Ensure that the “Quantity” field accepts numeric input only. | Critical | Failed | PS-004 |  |
| 24 | Ensure that users cannot add more than 5 of the same product per order. | Critical | Failed | PS-005 |  |
| 25 | Ensure that quantity validation occurs when a user enters a new quantity and presses Enter | High | Passed |  |  |
| 26 | Ensure that quantity validation occurs when a user enters a new quantity and clicks “Update Cart”. | High | Passed |  |  |
| 27 | Make sure the validation message “We’re sorry, but you can’t buy more than 5 items of this product.” appears when someone puts more than 5 items in their cart. | High | Failed | PS-005 |  |
| 28 | Make sure the validation message “We’re sorry, but we only have N items of this product available at the moment. Would you like to receive notifications when this product is available?” appears when the product is out of stock. | High | Failed | PS-006 |  |
| 29 | Make sure users can remove a product from their cart by clicking the “Remove” button next to the product’s price. | Critical | Passed |  |  |
| 30 | Make sure setting the quantity to 0 and clicking “Update Cart” removes the product from the cart. | Critical | Passed |  |  |
| 31 | Make sure users can’t add out-of-stock products to their cart. | Critical | Failed | PS-006 |  |
| 32 | Make sure a product added to the cart by a signed-in user remains visible across all sessions. | Critical | Passed |  |  |
| 33 | Make sure the cart is empty when a user signs out. | High | Passed |  |  |
| 34 | Make sure removing a product from the cart deletes it from all active sessions. | Critical | Passed |  |  |

## Bug reports

### PS-001 — Cart icon tooltip is not displayed when hovering over the cart icon.

| Field | Value |
|---|---|
| Preconditions | The user is on any page of the application. |
| Steps to reproduce | 1. Open the application.<br>2. Navigate to any page.<br>3. Hover over the cart icon. |
| Actual result | The tooltip does not appear when hovering over the cart icon. |
| Expected result | The tooltip “Carrinho” should be displayed when the user hovers over the cart icon. |
| Attachments | [screenrec](https://screenrec.com/share/CskB6hqiwE) |
| Notes | Issue observed on multiple pages. |
| Operating system | MacOS 14 (Sonoma) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Moderate |

### PS-002 — The “Name” column is missing from the cart page.

| Field | Value |
|---|---|
| Steps to reproduce | 1. Open the application.<br>2. Navigate to the cart page.<br>3. Check the table headers and available columns. |
| Actual result | The “Name” column is missing from the product table in the cart. |
| Expected result | The cart should display a table containing the following columns: Item ID, Product ID, Name, Description, In stock?, Quantity, List price and Total cost |
| Attachments | [screenshot](https://ibb.co/1GjXk774) |
| Operating system | MacOS 14 (Sonoma) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Major |

### PS-003 — The cart icon does not update to display the total quantity of added products.

| Field | Value |
|---|---|
| Preconditions | The user is on any page with products available for purchase. |
| Steps to reproduce | 1. Open the application.<br>2. Navigate to a product listing or product detail page (PDP).<br>3. Click the “Add to Cart” button on any product.<br>4. Observe the cart icon at the top of the page. |
| Actual result | The cart icon does not update to display the total number of items added to the cart. |
| Expected result | The cart icon should display a badge indicating the total number of products added to the cart. |
| Attachments | [screenshot](https://ibb.co/LXJZTp2v) |
| Notes | When a user adds a product to the cart, the cart icon should display a badge indicating the total number of items in the cart. However, this is not happening. |
| Operating system | MacOS 14 (Sonoma) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Major |

### PS-004 — The “Quantity” field allows non-numeric input.

| Field | Value |
|---|---|
| Preconditions | The user has at least one product added to the cart. |
| Steps to reproduce | 1. Open the application and add a product to the cart.<br>2. Navigate to the cart page.<br>3. Try to enter a non-numeric value (e.g., letters or symbols) in the “Quantity” field.<br>4. Observe the behavior of the input field. |
| Actual result | The “Quantity” field accepts non-numeric input. |
| Expected result | The “Quantity” field should only accept numeric input (whole numbers). |
| Attachments | [screenshot](https://ibb.co/gb3Qc1H3) |
| Operating system | MacOS 14 (Sonoma) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Major |

### PS-005 — Users are able to add more than 5 of the same product to the cart.

| Field | Value |
|---|---|
| Preconditions | The user has at least one product available for purchase. |
| Steps to reproduce | 1. Open the application and navigate to a product page.<br>2. Add a product to the cart.<br>3. In the “Quantity” field, enter a number greater than 5 (e.g., 6 or more).<br>4. Click “Update Cart” or proceed with adding the product.<br>5. Observe the system allows adding more than 5 items. |
| Actual result | The system allows the user to add more than 5 of the same product to the cart |
| Expected result | The system should prevent the user from adding more than 5 of the same product to the cart, either by showing a validation message or by limiting the input to 5. |
| Attachments | [screenshot](https://ibb.co/cK8hM50x) |
| Operating system | MacOS 14 (Sonoma) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Major |

### PS-006 — The validation message for out-of-stock products is not displayed when trying to add more items than available

| Field | Value |
|---|---|
| Preconditions | The product is out of stock. |
| Steps to reproduce | 1. Open the application and navigate to a product page that is out of stock.<br>2. Attempt to add the product to the cart.<br>3. Enter a quantity greater than the available stock (e.g., 2 when only 1 is available).<br>4. Observe if the validation message appears |
| Actual result | No validation message is displayed when attempting to add an out-of-stock product to the cart. |
| Expected result | The validation message should appear, informing the user of the limited stock and offering notification options for when the product becomes available:<br>“We’re sorry, but we only have N items of this product available at the moment. Would you like to receive notifications when this product is available?” |
| Attachments | [screenshot](https://ibb.co/SwKdqb0g) |
| Operating system | MacOS 14 (Sonoma) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Major |

### PS-007 — The validation message for out-of-stock products is not displayed when trying to add more items than available

| Field | Value |
|---|---|
| Preconditions | The product is out of stock. |
| Steps to reproduce | 1. Open the application and navigate to a product page that is out of stock.<br>2. Attempt to add the product to the cart.<br>3. Enter a quantity greater than the available stock (e.g., 2 when only 1 is available).<br>4. Observe if the validation message appears |
| Actual result | No validation message is displayed when attempting to add an out-of-stock product to the cart. |
| Expected result | The validation message should appear, informing the user of the limited stock and offering notification options for when the product becomes available:<br>“We’re sorry, but we only have N items of this product available at the moment. Would you like to receive notifications when this product is available?” |
| Attachments | [screenshot](https://ibb.co/SwKdqb0g) |
| Operating system | MacOS 14 (Sonoma) |
| App version | Demo |
| Browser | Chrome (latest) |
| Severity | Major |
