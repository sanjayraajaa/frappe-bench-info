# 📦 frappe-bench-info

A **simple CLI tool** to list all **Frappe/ERPNext benches, sites, and database sizes**.
It scans a given path, detects benches, and shows site details in a table – **no Frappe setup required**.

---

## ✅ Features
✔ Lists **Site Name, Bench Name, DB Name, DB Size (MB), Bench Path**  
✔ Detects benches inside a given path  
✔ Works without requiring Frappe to be running  

---

## 🚀 Installation

### 1️⃣ Download the `.deb` package (latest release)

```bash
wget https://github.com/sanjayraajaa/frappe-bench-info/releases/download/v1.1.1/frappe-bench-info_1.1.1.deb
````

### 2️⃣ Install the package

```bash
sudo dpkg -i frappe-bench-info_1.1.1.deb
sudo apt-get install -f   # Fix dependencies if required
```

---

## 🛠 Requirements

* Python 3
* PyMySQL (`pip install pymysql`)
* tabulate (`pip install tabulate`)
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
FRAPPE BENCH INFO TOOL
══════════════════════
+------------------+--------------+-------------------+----------------+-------------------------------+
| Site Name        | Bench Name   | DB Name           |   DB Size (MB) | Bench Path                    |
+==================+==============+===================+================+===============================+
| dev.frappe.local | frappe-bench | _05b9f72dad1c4928 |           43.2 | /home/sanjayraja/frappe-bench |
+------------------+--------------+-------------------+----------------+-------------------------------+
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
