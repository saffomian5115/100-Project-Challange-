# 💊 Pharma Inventory System

A modern pharmacy management desktop application built with Python and CustomTkinter — designed specifically for Pakistani pharmacies.

---

## 🖥️ Features

| Module | Description |
|---|---|
| 📊 Dashboard | Live stats, sales charts, stock distribution, top-selling medicines |
| 💊 Medicines | Add, edit, delete medicines with batch/expiry/vendor tracking |
| 📝 Billing | Fast POS billing with live medicine search and cart |
| 📄 Sales | View, filter, and print past bills |
| 🏢 Vendors | Manage suppliers and link them to medicines |
| 📦 Purchase Orders | Create orders, receive stock automatically |
| ⚠️ Alerts | Low stock, expiring soon, and expired medicine alerts with charts |
| 📈 Reports | Sales, stock, profit, and top-medicines reports with print support |
| ⚙️ Settings | Database backup/restore, mobile web server |
| 🌐 Mobile View | Flask web server for viewing dashboard and stock on mobile |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.9+
- Windows (tested), should work on Linux/macOS with minor tweaks

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/pharma-inventory.git
cd pharma-inventory

# Install dependencies
pip install -r requirements.txt

# Run the app
python main.py
```

### Default Login

```
Username: admin
Password: admin123
```

---

## 📦 Dependencies

```
customtkinter
pandas
reportlab
flask
```

Install all at once:

```bash
pip install customtkinter pandas reportlab flask
```

---

## 🗂️ Project Structure

```
pharma-inventory/
│
├── main.py                  # App entry point
├── database.py              # SQLite database layer
├── web_server.py            # Flask mobile web server
├── build_exe.py             # PyInstaller EXE build script
├── requirements.txt
│
├── gui/
│   ├── login.py             # Login screen
│   ├── dashboard.py         # Main dashboard with charts
│   ├── medicines.py         # Medicine management
│   ├── billing.py           # POS billing screen
│   ├── sales.py             # Sales history
│   ├── vendors.py           # Vendor management
│   ├── purchase_orders.py   # Purchase order management
│   ├── alerts.py            # Stock and expiry alerts
│   ├── reports.py           # Reports and analytics
│   └── settings.py          # App settings
│
├── web/
│   └── templates/
│       ├── dashboard.html   # Mobile dashboard
│       ├── stock.html       # Mobile stock view
│       └── reports.html     # Mobile reports (placeholder)
│
└── utils/
    ├── validators.py        # Input validation helpers
    └── helpers.py           # Common utility functions
```

---

## 🗄️ Database

The app uses **SQLite** and stores the database at:

```
C:\Users\<YourName>\AppData\Local\PharmaInventory\pharmacy.db
```

This location ensures the app works correctly even when installed in `Program Files`.

### Tables

- `users` — login accounts
- `medicines` — medicine inventory
- `vendors` — supplier details
- `bills` + `bill_items` — sales records
- `purchase_orders` + `purchase_order_items` — procurement
- `stock_transactions` — full audit trail of stock changes

---

## 📱 Mobile Web Server

View your pharmacy dashboard and stock on any phone on the same Wi-Fi:

1. Open **Settings** in the app
2. Click **🚀 Start Web Server**
3. Open the displayed URL on your phone (e.g. `http://192.168.1.5:5000`)

Or run it directly:

```bash
python web_server.py
```

---

## 🏗️ Building an EXE (Windows)

```bash
pip install pyinstaller
python build_exe.py
```

The executable will be created at `dist/PharmaInventory/PharmaInventory.exe`.

> **Note:** Copy your `pharmacy.db` to the `dist/PharmaInventory/` folder to carry over existing data.

---

## 💾 Backup & Restore

Go to **Settings → Backup & Restore**:

- **Backup Now** — saves a timestamped `.db` file to the `backups/` folder
- **Restore from Backup** — select any backup file to restore (requires app restart)

---

## 🌙 Theme

The app supports **Dark** and **Light** modes. Toggle using the button in the sidebar or on the login screen.

---

## 🔐 User Roles

Currently supports two roles:

- `admin` — full access
- `pharmacist` — standard access

User management can be extended via the `users` table in the database.

---

## 📄 License

This project is open source. Feel free to use and modify it for your own pharmacy.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first.

---

> Built with ❤️ for Pakistani pharmacies — currency set to **Rs.** by default.