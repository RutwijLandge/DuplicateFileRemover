# DuplicateFileRemover
A Python utility that scans directories to identify and delete duplicate files using MD5 checksums. Includes command-line options for help and usage. Ideal for cleaning up redundant files and saving disk space.
# 🧹 Duplicate File Remover

A Python utility script that scans a directory and deletes duplicate files based on their **MD5 checksum**. It helps clean up storage by identifying and removing redundant files.

---

## 🚀 Features

- ✅ Recursively scans all files in the given directory.
- 🔑 Computes MD5 checksum to detect duplicates based on **file content**, not filename.
- 🗑️ Deletes all duplicates, keeping only one copy.
- 🧾 Automatically logs operations with a timestamped log file (planned).
- 🆘 Supports command-line flags for help and usage instructions.

---

## 🛠️ How It Works

1. **CalculateChecksum**: Computes a checksum for each file using the MD5 algorithm.
2. **FindDuplicate**: Builds a dictionary of checksums and their associated files.
3. **DeleteDuplicate**: Deletes all but one file from each group of duplicates.

---

## 📦 Requirements

- Python 3.x  
- No external libraries required (uses built-in modules: `os`, `sys`, `hashlib`, `time`)

---

## 🧪 Usage

### ▶️ To run the script and delete duplicates:

```bash
python ScriptName.py /absolute/path/to/your/directory
python ScriptName.py --h   # Displays help message
python ScriptName.py --u   # Displays usage instructions

Sample Output - 
------------------------------------------------------
--------------- Marvellous Automation ----------------
------------------------------------------------------
Deleted file : /home/user/Documents/copy1.txt
Deleted file : /home/user/Documents/copy2.txt
Total Deleted File : 2
------------------------------------------------------
----------- Thank you for using our script -----------
---------------- Marvellous Infosystems --------------
------------------------------------------------------

