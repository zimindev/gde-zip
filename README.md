# **📚 Complete Archive Guide for CLI \ Linux (zip, unzip, p7zip) 🐧**

Manage your files like a pro! This guide covers **creating, extracting, and inspecting archives** using `zip`, `unzip`, and `p7zip` across all major Linux distros.

---

## **🛠 Installation on Different Distros**

### **Ubuntu/Debian 🐳**

```bash
sudo apt update
sudo apt install zip unzip p7zip-full
```

### **Fedora/RHEL 🎩**

```bash
sudo dnf install zip unzip p7zip p7zip-plugins
```

### **Arch Linux/Manjaro 🏗️**

```bash
sudo pacman -S zip unzip p7zip
```

### **OpenSUSE 🦎**

```bash
sudo zypper install zip unzip p7zip
```

---

## **🏁 Basic Usage**

### **Zip**

```bash
# Create a zip archive from a folder
zip -r archive.zip myfolder/

# Add files to an existing archive
zip archive.zip file1.txt file2.txt

# Update files in archive (add new/changed files)
zip -u archive.zip file.txt

# Exclude certain files
zip -r archive.zip myfolder/ -x "*.log" "*.tmp"
```

### **Unzip**

```bash
# Extract archive to current directory
unzip archive.zip

# Extract archive to a specific directory
unzip archive.zip -d /path/to/dir

# List contents of archive
unzip -l archive.zip

# Test archive for corruption
unzip -t archive.zip
```

### **p7zip (7z)**

```bash
# Create a 7z archive
7z a archive.7z myfolder/

# Create a zip archive using 7z
7z a archive.zip myfolder/

# Extract archive preserving paths
7z x archive.7z

# Extract to a specific directory
7z x archive.7z -o/path/to/dir

# List contents
7z l archive.7z
```

---

## **🎮 Quick Command Reference**

| Tool  | Command                      | Action          |
| ----- | ---------------------------- | --------------- |
| zip   | `zip -r archive.zip folder/` | Create archive  |
| zip   | `zip -u archive.zip file`    | Update archive  |
| unzip | `unzip archive.zip`          | Extract archive |
| unzip | `unzip -l archive.zip`       | List contents   |
| 7z    | `7z a archive.7z folder/`    | Create archive  |
| 7z    | `7z x archive.7z`            | Extract archive |
| 7z    | `7z l archive.7z`            | List contents   |

---

## **⚡ Advanced Tips**

```bash
# Create password-protected zip
zip -r -e secure.zip myfolder/

# Create highly compressed 7z archive
7z a -mx=9 archive.7z myfolder/

# Extract specific files from archive
unzip archive.zip file1.txt file2.txt
7z e archive.7z file1.txt file2.txt
```

---

## **🚀 Performance Tips**

* Use `-r` for recursive folders.
* Use `-mx=9` for maximum compression with 7z.
* Test archives after creation: `unzip -t` or `7z t`.
* Use 7z for large datasets or better compression ratios.

---

## 📚 **Additional Resources**

* **zip/unzip Official Docs**: [https://linux.die.net/man/1/zip](https://linux.die.net/man/1/zip)
* **p7zip Official Docs**: [https://www.7-zip.org/](https://www.7-zip.org/)
* **Community Forum**: [https://askubuntu.com/](https://askubuntu.com/)
