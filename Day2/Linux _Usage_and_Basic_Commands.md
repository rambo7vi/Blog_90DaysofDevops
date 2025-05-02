
# 🌐 Ways to Use Linux

Linux can be accessed and used through various environments depending on your requirements and resources:

### 1. 🖥️ Local OS Installation
- Install Linux directly on your laptop or desktop.
- Offers full performance and control.
- Common distributions: Ubuntu, Fedora, Arch, etc.

### 2. 📦 Virtual Machines (e.g., VirtualBox)
- Install Linux inside a VM on top of another OS.
- Safe for testing and learning.
- Easy to revert to snapshots.

### 3. 🐳 Vagrant / Docker
- Lightweight containers or VMs to run isolated Linux environments.
- Useful for development and testing.

### 4. 💻 WSL (Windows Subsystem for Linux)
- Run Linux natively inside Windows.
- WSL2 offers full Linux kernel support.
- Great for developers who need both Linux and Windows tools.

### 5. ☁️ Cloud Services (AWS, Azure, GCP)
- Spin up Linux virtual machines on the cloud.
- Scalable and remote access via SSH.
- Used for enterprise, web hosting, and development.

### 6. 🔀 Dual Boot Setup
- Install Linux alongside Windows or macOS.
- Choose your OS at boot time.
- Ideal for full-feature access on both systems.

---

# 📁 Linux Filesystem Overview

Linux uses a hierarchical file structure with a single root directory (`/`). Below are important folders:

- `/bin`: Essential user binaries (like `ls`, `cp`)
- `/boot`: Boot loader files (Linux kernel, initrd)
- `/dev`: Device files (e.g., disks, USB)
- `/etc`: Configuration files for the system
- `/home`: User directories (e.g., `/home/alice`)
- `/mnt`: Temporary mount points for filesystems
- `/media`: Mount points for removable media (USB, CD)
- `/opt`: Optional or third-party software
- `/root`: Home directory for root user
- `/sbin`: System binaries for administration
- `/tmp`: Temporary files (often cleared on reboot)
- `/var`: Variable data like logs, mail, spool files

---

# 📂 File & Folder Commands

### 📁 Creating Folders
```bash
mkdir myfolder                # Create directory
mkdir -p parent/child         # Create nested directories
```

### 📄 Creating Files
```bash
touch file.txt                # Create empty file
nano file.txt                 # Open in nano editor
vi file.txt                   # Open in vi editor
vim file.txt                  # Open in vim editor
```

### 🗑️ Deleting Files & Folders
```bash
rm file.txt                   # Delete file
rm -r myfolder                # Delete folder recursively
rmdir emptyfolder             # Delete empty folder
```

### 🔄 Moving & Renaming
```bash
mv oldname.txt newname.txt    # Rename file
mv file.txt /path/to/dir/     # Move file
```

### 📋 Copying Files & Folders
```bash
cp file.txt backup.txt        # Copy file
cp -r folder/ backup_folder/  # Copy folder recursively
```

---

📝 Use `man <command>` for detailed help. E.g., `man mkdir`

