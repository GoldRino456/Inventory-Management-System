<h1 align="center">Inventory Management System</h1>

<h3 align="center">A JavaFX desktop inventory management application for tracking parts and products with real-time CRUD operations and input validation.</h3>

<div align="center">
  
![Java](https://img.shields.io/badge/java-%23ED8B00?style=for-the-badge&logoColor=white)
![JavaFX](https://img.shields.io/badge/JavaFX-0078D7?style=for-the-badge&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)
![MIT License](https://img.shields.io/badge/MIT%20License-gray?style=for-the-badge)

</div>

## Key Features

- Part management: create, update, delete, and view InHouse and Outsourced parts
- Product management: create, update, delete, and view products
- Associate parts with products to track bill-of-materials relationships
- Search parts and products by ID or name
- Form validation for price, stock, and min/max inventory ranges
- Confirmation dialogs for destructive actions (delete part/product)
- Clean FXML-based user interface built with JavaFX

## Tech Stack

- Java 11
- JavaFX 11
- Maven

## Screenshots

### Inventory Main View

<img width="945" height="459" alt="InventoryScreen" src="https://github.com/user-attachments/assets/0c5c318e-2400-4426-9151-c7c72ebfb8f7" />

### Parts Screen

<img width="579" height="607" alt="PartModify" src="https://github.com/user-attachments/assets/8fd6d116-c8b0-47a6-be34-7a5a557e5280" />

### Products Screen

<img width="879" height="590" alt="ProductCreate" src="https://github.com/user-attachments/assets/9f9c6c43-ca81-4b21-886d-d442b20e6012" />

## Core Modules

### Main Dashboard

The `MainpageController` manages the primary inventory view, displaying all parts and products in searchable tables and routing the user to add or modify screens.

### Parts Management

`AddPartController` and `ModifyPartController` handle part creation and editing. The form supports both InHouse parts (with a machine ID) and Outsourced parts (with a company name), switching the bottom field based on the selected radio button.

### Products Management

`AddProductController` and `ModifyProductController` handle product creation and editing. Products can have associated parts added or removed from a separate table, and products with associated parts cannot be deleted until those parts are removed.

### Inventory & Domain Models

- `Inventory` — static inventory state with lookup, add, update, and delete methods
- `Part` — abstract base class for inventory parts
- `InHouse` — subclass of `Part` with a machine ID
- `Outsourced` — subclass of `Part` with a company name
- `Product` — product class with an associated list of parts

## Running It Locally

### Prerequisites

- Java 11 SDK
- Maven
- An IDE with JavaFX support (IntelliJ IDEA recommended)

### 1. Clone the Repository

```bash
git clone https://github.com/GoldRino456/Inventory-Management-System.git
```

### 2. Run the Application

```bash
mvn clean javafx:run
```

The inventory management dashboard will open.

## Project Architecture

```
Inventory Management System/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── inventorymgr/InventoryManagementSystem/
│   │   │   │   ├── Main.java
│   │   │   │   ├── MainpageController.java
│   │   │   │   ├── AddPartController.java
│   │   │   │   ├── ModifyPartController.java
│   │   │   │   ├── AddProductController.java
│   │   │   │   ├── ModifyProductController.java
│   │   │   │   ├── Inventory.java
│   │   │   │   ├── Part.java
│   │   │   │   ├── InHouse.java
│   │   │   │   ├── Outsourced.java
│   │   │   │   └── Product.java
│   │   │   └── module-info.java
│   │   └── resources/
│   │       └── inventorymgr/InventoryManagementSystem/
│   │           ├── inventory_mainpage.fxml
│   │           ├── inventory_addpart.fxml
│   │           ├── inventory_modifypart.fxml
│   │           ├── inventory_addproduct.fxml
│   │           └── inventory_modifyproduct.fxml
│   └── test/
├── pom.xml
├── .gitignore
└── README.md
```

## Author

Developed By: **Ethan H. Eastwood**

- Website: [EthanEastwood.dev](https://ethaneastwood.dev)
- Github: [@GoldRino456](https://github.com/GoldRino456)
- LinkedIn: [@ethan-h-eastwood](https://linkedin.com/in/ethan-h-eastwood)

A special thank you to **Western Governors University** for the opportunity and support throughout this project.
