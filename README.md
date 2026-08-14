# HandsMen Threads — Salesforce CRM

> A Salesforce CRM solution for managing customers, products, inventory, orders, and automated business processes for an apparel business.

## 📌 Project Overview

**HandsMen Threads** is a Salesforce-based CRM project designed to streamline customer, product, inventory, and order management.

The project demonstrates practical Salesforce concepts including **Custom Objects, Lightning App Builder, Salesforce Flows, Apex Triggers, Validation Rules, automation, relationships, and email notifications**.

## 🎯 Objectives

- Centralize customer and product information.
- Track inventory and stock availability.
- Manage customer orders through a structured lifecycle.
- Automatically calculate order totals.
- Send automated business notifications.
- Apply validation and business rules.
- Support customer loyalty management.
- Provide a user-friendly Lightning application.

## ✨ Key Features

### 👥 Customer Management
Stores customer name, email, phone, loyalty status, name details, and total purchases.

### 📦 Product Management
Manages product name, SKU, price, and stock quantity.

### 🏬 Inventory Management
Tracks inventory number, associated product, stock quantity, stock status, and warehouse information.

### 🛒 Order Management
Manages order number, customer, product, status, quantity, total amount, and customer email.

## ⚙️ Automation

### 1. Low Stock Alert
A record-triggered Flow detects low inventory and sends an email notification to the inventory manager.

### 2. Order Confirmation
When an order reaches the appropriate confirmation status, an automated confirmation email is sent.

### 3. Loyalty Program
Automation manages customer loyalty information based on purchasing activity.

### 4. Inventory / Stock Automation
Order processing can update inventory using:

```text
Updated Stock = Previous Stock − Ordered Quantity
```

## 💻 Apex Development

### Order Total Calculation

The project uses an Apex Trigger to calculate an order's total amount:

```text
Total Amount = Quantity × Product Price
```

Example:

```text
Quantity = 400
Price = $3
Total Amount = $1,200
```

### Apex Components

- **OrderTotalTrigger** — invokes order-total calculation logic when records are created or updated.
- **OrderTriggerHandler** — separates business logic from trigger events for cleaner, maintainable Apex code.

## 🧩 Salesforce Data Model

```text
HandsMen Customer
       │
       ▼
HandsMen Order ─────────► HandsMen Product
       │                         │
       │                         ▼
       └────────────────────► Inventory
```

### Main Custom Objects

| Object | Purpose |
|---|---|
| **HandsMen Customer** | Customer information |
| **HandsMen Product** | Product information |
| **HandsMen Order** | Customer orders |
| **Inventory** | Product stock |

## 🛠️ Technology Stack

| Technology | Usage |
|---|---|
| **Salesforce CRM** | Core platform |
| **Salesforce Lightning** | User interface |
| **Custom Objects** | Data modelling |
| **Salesforce Flow** | Business automation |
| **Apex** | Server-side business logic |
| **Apex Triggers** | Record-based automation |
| **Validation Rules** | Data validation |
| **Lightning App Builder** | Page/application customization |
| **Email Alerts** | Automated notifications |
| **Reports & Dashboards** | Business insights |

## 📊 Reports & Dashboards

The project can provide visibility into:

- Total orders
- Total sales
- Product stock levels
- Low-stock products
- Customer purchases
- Loyalty customers
- Order status distribution

## 🔐 Data Validation & Business Rules

Examples include:

- Validating order quantities based on order status.
- Preventing invalid order data.
- Maintaining required customer/product relationships.
- Applying business rules before records are saved.

## 🖥️ Lightning Application

The custom Salesforce application **HandsMen Threads** provides navigation for:

- HandsMen Customers
- HandsMen Orders
- HandsMen Products
- Inventories
- Marketing Campaigns
- Reports
- Dashboards
- Accounts
- Contacts

## 🔄 Example Business Process

```text
Customer places an order
          ↓
Order record is created
          ↓
Product and quantity are selected
          ↓
Order total is calculated
          ↓
Order status is updated
          ↓
Inventory is adjusted
          ↓
Confirmation email is sent
          ↓
Customer purchase information is updated
          ↓
Loyalty status is evaluated
```

## 💡 Future Enhancements

- Advanced inventory forecasting
- More sophisticated loyalty tiers
- Product-wise sales analytics
- Automated restock recommendations
- Apex test classes and expanded test coverage
- Enhanced dashboards
- Permission-set based access control
- Improved error handling and logging
- Salesforce DX source deployment
- CI/CD integration

## 👨‍💻 Author

**Pathikrit Pachal**

B.Tech — Electronics & Communication Engineering

Interested in **Software Development, Salesforce, Java, SQL, DSA, and Cloud Technologies**.

---

> **Built with Salesforce • Automated with Flow • Extended with Apex**
