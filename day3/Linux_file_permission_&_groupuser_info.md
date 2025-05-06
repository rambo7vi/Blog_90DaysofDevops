# Linux.md - Essential Linux Commands and Concepts  

##This guide summarizes key Linux commands and concepts for system management, web server setup, secure communication, and user/file administration.

## 1. Package Manager Commands

### Debian/Ubuntu (APT)

```bash
sudo apt update        # Update package index
sudo apt upgrade       # Upgrade installed packages
sudo apt install <package>   # Install a package
sudo apt remove <package>    # Remove a package
```

### RedHat/CentOS (YUM/DNF)

```bash
sudo yum update        # Update all packages
sudo yum install <package>
sudo yum remove <package>

# or with DNF (modern alternative to yum)
sudo dnf install <package>
```

---

## 2. systemctl Commands (Systemd Services)

```bash
sudo systemctl start <service>     # Start service
sudo systemctl stop <service>      # Stop service
sudo systemctl restart <service>   # Restart service
sudo systemctl enable <service>    # Enable service at boot
sudo systemctl status <service>    # Check service status
```

---

## 3. NGINX Configuration

* Main HTML files are located at:

```bash
/var/www/html
```

* Upload your `.html` file here to serve via NGINX.
* NGINX configuration file:

```bash
/etc/nginx/nginx.conf
```

* Restart NGINX after making changes:

```bash
sudo systemctl restart nginx
```

---

## 4. Basic Linux Commands

```bash
uname -a        # System information
umask           # Show default file permission mask
whoami          # Show current logged-in user
cat <file>      # Display file contents
```

---

## 5. User Management

### Add User

```bash
sudo useradd <username>
sudo passwd <username>    # Set password for user
```

### Switch User

```bash
su - <username>           # Switch to another user
```

---

## 6. SSH Access with Public/Private Key

### Step-by-Step:

1. On the **local system**, generate keys:

```bash
ssh-keygen
```

* This creates:

  * Private key: `~/.ssh/id_rsa`
  * Public key: `~/.ssh/id_rsa.pub`

2. Copy the **public key** to the **remote server**:

```bash
ssh-copy-id user@remote_ip
```

* OR manually copy contents of `id_rsa.pub` into:

```bash
~/.ssh/authorized_keys    # on the remote server
```

3. Connect using private key:

```bash
ssh -i ~/.ssh/id_rsa user@remote_ip
```

---

## 7. SCP (Secure Copy)

Used to copy files between systems securely.

### Syntax:

```bash
scp /path/to/localfile user@remote_ip:/remote/path
scp user@remote_ip:/remote/file /local/path
```

---

## 8. Users and Groups

### Create Group

```bash
sudo groupadd <groupname>
```

### Add User to Group

```bash
sudo usermod -aG <groupname> <username>
# OR
sudo gpasswd -a <username> <groupname>
```

### Lock/Unlock User

```bash
sudo passwd -l <username>    # Lock user
sudo passwd -u <username>    # Unlock user
```

---

## 9. File Ownership and Permissions

### Check Permissions

```bash
ls -l filename
```

Output:

```
-rwxrwxrwx
```

Each set of `rwx` is for:

* User
* Group
* Others

### Change Ownership

```bash
sudo chown user:group filename
```

### Change Group

```bash
sudo chgrp <group> filename
```

### Change Permissions with Binary (Octal) Notation

```bash
chmod 764 filename
```

* `7` = `rwx` (4+2+1)
* `6` = `rw-` (4+2)
* `4` = `r--` (4)

So `764` means:

* Owner: read, write, execute
* Group: read, write
* Others: read

---
