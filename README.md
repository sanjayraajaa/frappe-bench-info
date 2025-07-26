# 📦 frappe-bench-info

A **CLI tool** that lists all **Frappe/ERPNext benches, sites, and database sizes** on a server or in development environments.
It scans the specified path, detects all benches, and displays site details in a table.
---

## ✅ Features
✔ Lists **Site Name, Bench Name, DB Name, DB Size (MB), Bench Path**  
✔ Detects benches inside a given path  
✔ Works without requiring Frappe to be running  

---

## 🚀 Installation

### 1️⃣ Download the `.deb` package (latest release)

```bash
wget https://github.com/sanjayraajaa/frappe-bench-info/releases/download/v1.0.0/frappe-bench-info_1.0.0.deb
````

### 2️⃣ Install the package

```bash
sudo dpkg -i frappe-bench-info_1.0.0.deb
sudo apt-get install -f   # Fix dependencies if required
```

---

## 🛠 Requirements

* Python 3
* PyMySQL (`pip install pymysql`)
* MariaDB/MySQL running
* User must have access to `information_schema`

---

## 🔥 Usage

Run the tool with:

```bash
frappe-bench-info --start_path /path/to/search [--db_user root] [--db_host localhost]
```

You will be asked to **enter the MariaDB/MySQL password**.

---

### Example

```bash
frappe-bench-info --start_path /home/frappe
```

🔑 The script will prompt for the password.

---

### Example Output

```
Site Name                 Bench Name           DB Name                        DB Size (MB)    Bench Path
---------------------------------------------------------------------------------------------------------------------
dev.local                 frappe-bench         _05b9f72dad1c4928              43.20           /home/frappe/frappe-bench
test.local                frappe-bench         _a83df921d72bcb39              22.50           /home/frappe/frappe-bench
```

---

## 📂 Development

Clone the repo:

```bash
git clone https://github.com/sanjayraajaa/frappe-bench-info.git
cd frappe-bench-info
```

Run directly (without installing):

```bash
python3 usr/local/bin/frappe-bench-info --start_path /home/frappe
```

---

## 📝 License

MIT License © 2025 **Sanjay Raja S**
