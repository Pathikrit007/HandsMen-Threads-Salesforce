# HandsMen Threads — Salesforce CRM

> A Salesforce CRM solution for managing customers, products, inventory, orders, and automated business processes for an apparel business.

## 📌 Project Overview

**HandsMen Threads** is a Salesforce-based CRM project designed to streamline customer, product, inventory, and order management.

The project demonstrates practical Salesforce concepts including **Custom Objects, Lightning App Builder, Salesforce Flows, Apex Triggers, Validation Rules, automation, relationships, and email notifications**.

## 📸 Project Preview

![HandsMen Threads Salesforce Application](ScreenShots/Custom%20App%20for%20Handsmen%20Threads.jpg)

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

The project uses Apex Triggers to automate important order and inventory operations.

### 1. Order Total Calculation

The `Order_Total_Trigger` automatically calculates the total amount of an order using the product price and ordered quantity.

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

- **Order_Total_Trigger** — invokes order-total calculation logic when records are created or updated.
- **Stock_Deduction_Trigger** — Deducts the ordered quantity from the related inventory when an order is confirmed.

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

| Technology / Feature | Purpose |
|---|---|
| **Salesforce CRM** | Core CRM platform for managing business data and processes |
| **Salesforce Lightning** | User interface and application experience |
| **Custom Objects & Fields** | Data modelling for customers, products, orders, and inventory |
| **Salesforce Flow** | Declarative automation and business process management |
| **Apex** | Programmatic business logic |
| **Apex Triggers** | Automated order and inventory operations |
| **Validation Rules** | Enforcing business rules and maintaining data integrity |
| **Email Alerts** | Automated customer and inventory notifications |
| **Lightning App Builder** | Building and customizing application pages |
| **Reports & Dashboards** | Monitoring business and operational information |

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

## 📸 Project Demonstration

### 🖥️ HandsMen Threads Salesforce Application

<p align="center">
  <img src="ScreenShots/Custom%20App%20for%20Handsmen%20Threads.jpg" alt="HandsMen Threads Salesforce Application" width="600">
</p>

### 👥 Customer Management

<p align="center">
  <img src="ScreenShots/Customer%20Creation%20in%20HandsMen%20Thread.png" alt="Customer Management" width="600">
</p>

### 📦 Product Management

<p align="center">
  <img src="ScreenShots/Products%20in%20HandsMen%20Threads.png" alt="Product Management" width="600">
</p>

### 🏬 Inventory Management

<p align="center">
  <img src="ScreenShots/Inventories%20In%20Handsmen%20Thread.png" alt="Inventory Management" width="600">
</p>

### 🛒 Order Management

<p align="center">
  <img src="ScreenShots/Order%20confirmation.png" alt="Order Management" width="600">
</p>

### ⚙️ Automation & Flows

#### Order Confirmation Flow

<p align="center">
  <img src="ScreenShots/Order%20Confirmation%20Flow.jpg" alt="Order Confirmation Flow" width="500">
</p>

#### Stock Alert Flow

<p align="center">
  <img src="ScreenShots/Stock%20Alert%20Flow.jpg" alt="Stock Alert Flow" width="500">
</p>

### 📧 Automated Notifications

#### Low Stock Alert

<p align="center">
  <img src="ScreenShots/Low%20Stock%20Alert%20Email.png" alt="Low Stock Alert Email" width="500">
</p>

#### Order Confirmation Email

<p align="center">
  <img src="ScreenShots/Order%20Confirmation%20Email.png" alt="Order Confirmation Email" width="500">
</p>

#### Loyalty Program Email

<p align="center">
  <img src="ScreenShots/Loyalty%20Program%20Email.jpg" alt="Loyalty Program Email" width="500">
</p>

> 📌 Additional screenshots related to setup, configuration, validation rules, and other implementation details are available in the [`ScreenShots`](ScreenShots/) folder.

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
