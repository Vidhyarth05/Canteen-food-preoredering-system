# Canteen Management System

A comprehensive Python-based solution for managing a school or college canteen, featuring separate interfaces for students and administrators, digital wallet integration, and a complete food ordering system.

##  Overview

This Canteen Management System provides an efficient way to handle daily canteen operations. It allows students to browse menu items, place orders, and manage their canteen card/wallet balance. Administrators can manage the menu, update prices, and handle student wallet balances.

##  Features

### For Students
- **User Authentication**: Secure login with username and password
- **Menu Browsing**: View available food items with descriptions and prices
- **Shopping Cart**: Add items to cart, view cart contents, and modify quantities
- **Multiple Payment Options**: Pay using canteen card, digital wallet, or cash
- **Order History**: Review past orders and expenses
- **Wallet Management**: Check wallet balance

### For Administrators
- **Menu Management**: Add, update, or remove menu items
- **Price Management**: Update pricing for existing items
- **Student Wallet Management**: Add or subtract funds from student wallets
- **Canteen Operations**: Complete control over the canteen system

##  Technical Details

### Classes Structure
- **User**: Base class for authentication and user information
- **Student**: Extended user class with student-specific functionality
- **Admin**: Extended user class with administration privileges
- **FoodItem**: Represents menu items with details
- **Menu**: Manages the collection of food items
- **Cart**: Handles the shopping cart functionality
- **Order**: Processes and records orders

### Exception Handling
Custom exception classes:
- `CanteenException`: Base exception class
- `InsufficientBalanceException`: For payment failures
- `InvalidPasswordException`: For authentication failures
- `UserNotFoundException`: For user lookup failures

##  File Structure
- `users.txt`: Stores user credentials and roles
- `wallet.txt`: Maintains student wallet balances
- `food_items.txt`: Contains the menu items data
- `bill_history.txt`: Keeps record of all transactions

### File Formats

#### users.txt
Format: `username|password|role|additional_info|balance|wallet_password`

Examples:
```
admin1|admin123|admin|Main Canteen
student1|pass123|student|S123456|500.00|wallet123
```

#### wallet.txt
Format: `student_id|balance`

Example:
```
S123456|150.50
S789012|75.25
```

#### food_items.txt
Format: `item_id|name|description|price|availability`

Example:
```
1|Sandwich|Fresh vegetable sandwich|50.00|True
2|Pasta|Creamy white sauce pasta|80.00|True
```

#### bill_history.txt
Format: `student_id|items_details|total_price`

Example:
```
S123456|2x Sandwich; 1x Pasta|180.00
```
### Student Interface
1. Login with student credentials
2. Choose from options:
   - View menu
   - Add items to cart
   - View cart
   - Place order
   - View order history
   - Check wallet balance

### Admin Interface
1. Login with admin credentials
2. Choose from options:
   - Add new menu items
   - Show menu items
   - Update prices
   - Remove items
   - Update student wallet balances

##  Security Features
- Password protection for user accounts
- Separate wallet password for transactions
- Exception handling for secure transactions

##  Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

##  License
This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Authors
- Syed Faazil - Initial work
- Vidhyarth
