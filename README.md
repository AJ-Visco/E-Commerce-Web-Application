# 🛒 TechHub Electronics – Online Store

A front-end e-commerce simulation built with vanilla HTML, CSS, and JavaScript as part of **CMIS-3500 Web Programming I – Project 6**.

---

## 📋 Project Overview

TechHub Electronics is a single-page online storefront that allows users to browse a product catalog, manage a shopping cart, and complete a checkout process with billing, delivery, and payment information. The entire application runs client-side with no frameworks or external dependencies.

---

## ✨ Features

- **Product Catalog** – Dynamically rendered product cards with emoji icons, names, prices, and quantity selectors
- **Shopping Cart** – Add items with custom quantities, view line-item totals, and remove individual products
- **Live Cart Total** – Running order total that updates instantly as items are added or removed
- **Checkout Form** – Multi-section form covering:
  - Billing address (name, email, phone, street, city, state, ZIP)
  - Delivery address with a *Same as Billing* auto-fill checkbox
  - Payment information (card number, cardholder name, expiry, CVV)
- **Client-Side Form Validation** – Inline error messages for every required field with format checks (email regex, 10-digit phone, 16-digit card number, MM/YY expiry, 5-digit ZIP, 2-letter state code)
- **Input Formatting** – Auto-formatting for phone numbers `(XXX) XXX-XXXX`, credit card numbers `XXXX XXXX XXXX XXXX`, and expiry dates `MM/YY`
- **Order Confirmation Modal** – Animated modal displaying order total, item count, and a randomly generated order ID
- **Responsive Design** – CSS Grid layout that adapts from a two-column desktop view to a single-column mobile layout via media queries

---

## 🗂️ File Structure

```
.
└── CMIS3500_P6_AJ_Visco.html   # Single self-contained HTML file (markup, styles, logic)
```

All CSS is written in a `<style>` block and all JavaScript is written in a `<script>` block within the same HTML file — no external files required.

---

## 🚀 Getting Started

No build tools, package managers, or servers are needed.

1. Clone or download the repository.
2. Open `CMIS3500_P6_AJ_Visco.html` in any modern web browser.
3. That's it — the app runs entirely in the browser.

```bash
git clone https://github.com/AJ-Visco/E-Commerce-Web-Application.git
cd E-Commerce-Web-Application
# Open the HTML file in your browser
open CMIS3500_P6_AJ_Visco.html
```

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and form elements |
| CSS3 | Styling, CSS Grid layout, animations, responsive design |
| Vanilla JavaScript (ES6+) | DOM manipulation, cart logic, form validation, event handling |

---

## 📐 Application Flow

```
Product Catalog → Add to Cart → Shopping Cart → Proceed to Checkout → Fill Form → Submit → Order Confirmation Modal → Reset
```

1. Products are rendered dynamically from a JavaScript array on page load.
2. Users select a quantity and click **Add to Cart**; the cart panel updates in real time.
3. Clicking **Proceed to Checkout** reveals the checkout form below the cart.
4. On submission, all fields are validated; errors scroll into view automatically.
5. A successful submission displays an order confirmation modal with a generated order ID.
6. Closing the modal resets the cart and form, returning the user to the catalog.

---

## ✅ Form Validation Rules

| Field | Rule |
|---|---|
| Full Name | Minimum two words (first + last) |
| Email | Standard email format (`x@x.x`) |
| Phone | Exactly 10 digits |
| Street Address | Minimum 5 characters |
| City | Letters and spaces only, minimum 2 characters |
| State | Exactly 2 letters (e.g., `CA`) |
| ZIP Code | Exactly 5 digits |
| Card Number | Exactly 16 digits |
| Expiry Date | `MM/YY` format, must be a future date |
| CVV | 3 or 4 digits |

---

## 👤 Author

**AJ Visco**  
CMIS-3500 Web Programming I – Project 6
