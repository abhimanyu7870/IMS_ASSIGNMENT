Here is a possible `README.md` file for the given code:

---

# Inventory Management System

This project is an Inventory Management System that allows users to view product details, purchase items, update inventory, generate sales records, and add new items into the inventory. The system is implemented in Python, and data is stored in JSON format for persistence.

## Features
1. **View Product Details**: Display product information such as name, price, brand, category, and available quantity.
2. **Purchase Items**: Users can purchase products by specifying the product ID and quantity. The inventory is updated after each purchase.
3. **Generate Sales Record**: After a purchase, a sales record is created with details of the product and the total bill, which is stored in a JSON file.
4. **Add New Item**: Users can add new items to the inventory with details such as product name, price, weight, brand, category, and quantity.
5. **Update Inventory**: Inventory is updated after every purchase, and the updated inventory is saved to the `record.json` file.

## File Structure
- `record.json`: Stores product details and inventory.
- `sales.json`: Stores sales records after each purchase.

## Prerequisites
- Python 3.x
- JSON module (included by default with Python)

## Usage

### 1. **Read Data from JSON**
   This step reads product details from `record.json` to display available items and their details.

### 2. **Purchase an Item**
   - Input product ID and quantity.
   - Displays product name, price, and calculates the total bill.
   - Updates the inventory after the purchase.

### Example:
```python
Enter the product_Id: 109
Enter the quantity: 5
Product name:  5-star
Price:  60
```

### 3. **Generate Sales Record**
   After a purchase, the system generates a sales record with details of the product, quantity purchased, and total price. This record is stored in the `sales.json` file.

### Example Sales Record:
```json
{
    "1": {"Product_id": "109", "Quantity": 5, "Total bill": 60},
    "2": {"Product_id": "109", "Quantity": 5, "Total bill": 60}
}
```

### 4. **Add New Item to Inventory**
   Users can add new products to the inventory by specifying details like product name, price, weight, brand, category, and quantity. The new product is then added to the `record.json` file.

### Example:
```python
Enter product id: 141
Enter Product name: Pani Puri
Enter price: 20
Enter Weight: 500
Enter the brand name: Haldiram
Enter Category: Pani Puri
Enter Quantity: 1000
```

### 5. **Delete Item from Inventory**
   The system allows deleting products from the inventory by specifying the product ID to remove it from `record.json`.

### Example:
```python
del record['101']
```

## File Handling
- After every operation, the system writes updated data back to the respective JSON files (`record.json` and `sales.json`).

## Notes
- Ensure that the `record.json` and `sales.json` files are properly formatted and exist in the same directory as the script for the program to work correctly.
- The script uses the Python `json` module to read and write JSON data.

---
