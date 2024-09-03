# Inventory Management System

This SQL project creates a database for an Inventory Management System, including tables for Suppliers, Products, and Restock Orders. It also inserts sample data and demonstrates various queries and operations such as selecting, updating, and deleting records.

## Database Structure

- **Suppliers**: Stores information about suppliers, including Name, Contact, and Phone.
- **Products**: Stores details of products, including Name, Description, Stock Quantity, Price, and a SupplierID referencing the Suppliers table.
- **Restock Orders**: Stores restock orders, including the product, quantity, and order date.

## Created Tables

1. **Suppliers**
    - `SupplierID` (INT, PK, Auto Increment)
    - `Name` (VARCHAR(100), NOT NULL)
    - `Contact` (VARCHAR(100))
    - `Phone` (VARCHAR(20))

2. **Products**
    - `ProductID` (INT, PK, Auto Increment)
    - `Name` (VARCHAR(100), NOT NULL)
    - `Description` (TEXT)
    - `StockQuantity` (INT, DEFAULT 0)
    - `Price` (DECIMAL(10, 2), NOT NULL)
    - `SupplierID` (INT, FK, REFERENCES Suppliers)

3. **Restock Orders**
    - `OrderID` (INT, PK, Auto Increment)
    - `ProductID` (INT, FK, REFERENCES Products)
    - `Quantity` (INT, NOT NULL)
    - `OrderDate` (DATE, NOT NULL)

## Data Insertion

- Suppliers: Includes 3 suppliers with their names, contacts, and phone numbers.
- Products: Includes 3 products with names, descriptions, stock quantities, prices, and supplier IDs.
- Restock Orders: Records 3 restock orders for the products.

## Queries and Operations

1. **Select all products in stock**:
   ```sql
   SELECT * FROM Products;
