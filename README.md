# 📦 frappe-bench-info

A simple **CLI tool** to check the **database sizes of all Frappe/ERPNext sites** across multiple benches.

It lists:

✅ **Site Name**
✅ **Bench Name**
✅ **Database Name**
✅ **Database Size (MB)**
✅ **Total DB Size per Bench**

---

## 🚀 Installation

### 1️⃣ Download the `.deb` package (latest release)

```bash
wget https://github.com/sanjayraajaa/frappe-bench-info/releases/download/v1.0.0/frappe-bench-info_1.0.0.deb
```

### 2️⃣ Install the package

```bash
sudo dpkg -i frappe-bench-info_1.0.0.deb
sudo apt-get install -f   # Fix dependencies if required
```

---

## 🛠 Dependencies

The package automatically installs **PyMySQL** if not available.
It requires:

* Python 3
* MariaDB/MySQL running
* Permissions to access `information_schema`

---

## 🔥 Usage

Run the tool with:

```bash
frappe-bench-info --db_password <DB_PASSWORD> [--db_user root] [--db_host localhost] [--start_path /path/to/search]
```

### Example

```bash
frappe-bench-info --db_password 12345 --start_path /home/frappe
```

### Output

```
Site Name                 Bench                DB Name                        DB Size (MB)
-----------------------------------------------------------------------------------------------
dev.local                 frappe-bench         _05b9f72dad1c4928              43.20

Total DB Size per Bench:
-----------------------------------
frappe-bench         43.20 MB
```

---

## 📂 Development

Clone the repo:

```bash
git clone https://github.com/sanjayraajaa/frappe-bench-info.git
cd frappe-bench-info
```

Run directly (without .deb):

```bash
python3 usr/local/bin/frappe-bench-info --db_password <password> --start_path /home/frappe
```

---

## 📝 License

MIT License © 2025 **Sanjay Raja S**

---

Do you want me to **add usage examples with screenshots and a build/install guide for contributors** too?
