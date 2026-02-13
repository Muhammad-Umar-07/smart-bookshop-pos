# 📚 Smart Book Shop Management & Billing System

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey)
![CustomTkinter](https://img.shields.io/badge/GUI-CustomTkinter-ff69b4)

A professional, user-friendly Point of Sale (POS) system designed specifically for book shops and school book sellers. Built with Python and CustomTkinter, it offers a modern interface for inventory management, billing, and sales reporting.

----------------------------------------------------------------

## 📑 Table of Contents

- [Features](#-features)
- [Built With](#-built-with)
- [Requirements](#-requirements)
- [Installation](#-installation)
- [Default Login](#-default-login)
- [Folder Structure](#-folder-structure)
- [How to Use](#-how-to-use)
- [Tips for Best Use](#-tips-for-best-use)
- [Data Safety](#-data-safety)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)
- [Support](#-support)

----------------------------------------------------------------

## ✨ Features

### 🔐 Secure Authentication
- Simple staff login system with password protection
- Change password option for security
- Secure logout functionality

----------------------------------------------------------------

### 📦 Inventory Management
- **Add Books**: Easy form to add new books with title, SKU, category (class 9–12), and price
- **Edit Books**: Update existing book information
- **Delete Books**: Remove books with confirmation
- **View Books**: Professional table view with search and filter options (by class, title, or SKU)

----------------------------------------------------------------

### 🛒 Sales & Billing
- Simple point-of-sale interface
- Add books to cart in any order
- Real‑time total calculation (in **Rs** – Indian Rupees)
- Shopping cart management (add/remove items, clear cart)
- Professional invoice generation with date, time, and itemised details
- All sales automatically saved to daily Excel files

----------------------------------------------------------------

### 📊 Sales Reports
- Automatic daily Excel file generation (`DD-MM-YYYY.xlsx`)
- Each file contains:
  - Date & time of sale
  - Book title
  - Class/category
  - SKU / serial number
  - Unit price (Rs)
  - Total bill (Rs)
- View historical sales reports with a clean table interface
- Professionally formatted Excel files with headers and column widths

----------------------------------------------------------------

### 🎨 User Interface
- Clean, modern design using **CustomTkinter**
- Large, readable text and clear buttons
- **Back button** in every menu for easy navigation
- Minimal typing required – ideal for users with basic computer skills

----------------------------------------------------------------

## 🛠️ Built With

- [Python 3.8+](https://www.python.org/) – Core programming language
- [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter) – Modern UI toolkit
- [OpenPyXL](https://openpyxl.readthedocs.io/) – Excel file generation and formatting
- [Pandas](https://pandas.pydata.org/) – Data manipulation and Excel handling
- [JSON](https://docs.python.org/3/library/json.html) – Lightweight data storage for inventory and credentials

----------------------------------------------------------------

## 📋 Requirements

- **Python 3.8 or higher** installed on your system
- Operating system: Windows, macOS, or Linux

----------------------------------------------------------------

## 🚀 Installation

### Step 1: Install Python
If you don't have Python installed:
- Download from [python.org](https://www.python.org/downloads/)
- During installation, **check** “Add Python to PATH”

### Step 2: Install Dependencies
Open a terminal/command prompt in the project folder and run:

```bash
pip install -r requirements.txt
```

Contents of requirements.txt:
```
customtkinter
openpyxl
pandas
```

### Step 3: Run the Application
```bash
python bookshop_system.py
```

----------------------------------------------------------------

## 🔑 Default Login

| Credential   | Value       |
|--------------|-------------|
| **Password** | `admin123`  |

> ⚠️ **Important:** Change this password immediately after your first login!

----------------------------------------------------------------

## 📁 Folder Structure

The system automatically creates these folders on first run:

```
BookShopSystem/
├── bookshop_system.py          # Main application
├── requirements.txt            # Dependencies
├── README.md                   # This file
├── Inventory/                  # Book database storage
│   └── books.json              # JSON file with all books
├── Sales_Records/              # Daily sales Excel files
│   ├── 13-02-2026.xlsx         # Example: today's sales
│   ├── 14-02-2026.xlsx         # Example: tomorrow's sales
│   └── ...
└── Application_Files/          # System configuration
    └── credentials.json         # Staff password (stored securely)
```

----------------------------------------------------------------

## 📖 How to Use

### First Time Setup
1. **Run the application**:
   ```bash
   python bookshop_system.py
   ```
2. **Login** with the default password: `admin123`
3. **Change Password**:
   - From the main menu, click **“Change Password”**
   - Enter current password, then a new password twice
   - Click **“Change Password”**

----------------------------------------------------------------

### Adding Books to Inventory
1. From the main menu, click **“Inventory Management”**
2. Click **“Add New Book”**
3. Fill in the form:
   - **Book Title**: e.g., “Mathematics Textbook”
   - **SKU / Serial Number**: e.g., “MATH-9-001” (must be unique)
   - **Category/Class**: Must be `9`, `10`, `11`, or `12`
   - **Unit Price**: e.g., `450` (will be displayed as **Rs 450**)
4. Click **“Add Book”** – you'll see a success message.

----------------------------------------------------------------

### Making a Sale
1. From the main menu, click **“New Sale”**
2. **Left Panel – Available Books**:
   - Browse all available books
   - Use **“Filter by Class”** dropdown to filter by class
   - Click on any book to add it to the cart
3. **Right Panel – Shopping Cart**:
   - View selected books with real‑time total in **Rs**
   - Remove items using the **×** button
   - Click **“Clear Cart”** to remove all items
4. Click **“Generate Invoice”** when ready
5. A professional invoice is displayed with all details
6. The sale is automatically saved to the daily Excel file in `Sales_Records/`

----------------------------------------------------------------

### Viewing Sales Reports
1. From the main menu, click **“Sales Reports”**
2. A list of all daily Excel files appears (most recent first)
3. Click **“View Report”** next to any date
4. The report opens in a table view showing every transaction

----------------------------------------------------------------

### Editing Books
1. Go to **Inventory Management** → **“Edit Book”**
2. Select the book you want to edit from the list
3. Update any information in the form
4. Click **“Save Changes”**

----------------------------------------------------------------

### Deleting Books
1. Go to **Inventory Management** → **“Delete Book”**
2. Find the book and click its **“Delete”** button
3. Confirm the deletion when prompted

----------------------------------------------------------------

## 💡 Tips for Best Use

### Daily Operations
- **Start of day**: Log in with your password.
- **During sales**: Keep the **“New Sale”** screen open for quick transactions.
- **Add multiple items**: Books can be added to the cart in any order.
- **End of day**: Check **Sales Reports** to review the day's transactions.

----------------------------------------------------------------

### Inventory Management
- Use clear, consistent naming for books.
- Create unique SKU codes (e.g., `MATH-10-001`, `ENG-11-002`).
- Regularly update prices if needed.
- Use the **search** function to quickly find books.

----------------------------------------------------------------

### Security
- Change the default password immediately.
- Don't share your password.
- Always **log out** when leaving the computer.
- Periodically back up the `Inventory/books.json` file.

----------------------------------------------------------------

## 🛡️ Data Safety

- **Book inventory** is saved in JSON format in `Inventory/books.json`
- **Sales records** are saved as Excel files in `Sales_Records/`
- **Credentials** are stored in `Application_Files/credentials.json`
- **Backup tip**: Regularly copy these folders to a safe location (e.g., cloud storage, external drive)

----------------------------------------------------------------

## 🔧 Troubleshooting

| Problem                          | Solution                                                                                       |
|----------------------------------|------------------------------------------------------------------------------------------------|
| Application won't start          | Ensure Python is installed (`python --version`). Install dependencies with `pip install -r requirements.txt`. |
| Can't log in (forgot password)   | Delete the `Application_Files/credentials.json` file to reset to default password `admin123`. |
| Excel files not generating        | Check that you have write permissions in the folder. Run `pip install openpyxl pandas` to ensure libraries are installed. |
| Books not showing in inventory    | Verify that `Inventory/books.json` exists. Try adding a new book to initialise the system.    |
| "SKU already exists" error        | Choose a unique SKU for each book.                                                             |
| Excel files won't open            | You need Microsoft Excel, LibreOffice Calc, or another spreadsheet viewer installed.           |

----------------------------------------------------------------

## 🤝 Contributing

Contributions are welcome! If you'd like to improve this project:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

Please ensure your code follows the existing style and includes appropriate comments.

----------------------------------------------------------------

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

----------------------------------------------------------------

## 📞 Support

For issues or questions:
- Check this README thoroughly.
- Verify that all dependencies are installed.
- Review any error messages in the terminal.
- If the problem persists, please open an issue on the [GitHub repository](https://github.com/yourusername/book-shop-management).

----------------------------------------------------------------

**Made with ❤️ for Book Sellers**  
*Professional • Simple • Reliable*

----------------------------------------------------------------
