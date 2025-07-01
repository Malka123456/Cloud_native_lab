## **Introduction to basic and essential Linux commands.**


## **Terminal Basics**  

### **1. What is a Terminal?**  
- A **terminal emulator** is a program that provides a **command-line interface (CLI)** in a graphical environment.  
  - Examples:  
    - **Mac**: Terminal, iTerm2  
    - **Windows**: PuTTY  
    - **Linux**: Terminal, xterm, KDE Konsole  

### **2. What is a Shell?**  
- A **shell** is a **command interpreter** that takes user commands and executes them.  
- Common shells:  
  - `bash` (Bourne Again Shell)  
  - `zsh` (Z Shell, default on macOS)  
  - `sh` (Bash predecessor)  
  - `fish` (Friendly Interactive Shell)  

### **3. Command Prompt Structure**  
Example:  
```
root@hostname:/current/directory$  
```  
- **root**: Current user  
- **hostname**: Name of the machine/server  
- **/current/directory**: Present working directory  

---

## **Basic Commands**  

### **1. Navigation & File Operations**  
| Command | Description | Example |
|---------|------------|---------|
| `pwd` | Print current directory | `pwd` |
| `ls` | List files/folders | `ls -a` (show hidden) |
| `cd` | Change directory | `cd Downloads` |
| `mkdir` | Create directory | `mkdir folder_name` |
| `touch` | Create empty file | `touch file.txt` |
| `cp` | Copy file/folder | `cp file.txt copy.txt` |
| `mv` | Move/rename file | `mv old.txt new.txt` |
| `rm` | Remove file | `rm file.txt` |
| `rm -r` | Remove directory | `rm -r folder/` |

### **2. File Viewing & Editing**  
| Command | Description | Example |
|---------|------------|---------|
| `cat` | Display file content | `cat file.txt` |
| `head` | Show first N lines | `head -5 file.txt` |
| `tail` | Show last N lines | `tail -3 file.txt` |
| `vim` | Edit file (Vim editor) | `vim file.txt` |
| `nano` | Edit file (Nano editor) | `nano file.txt` |

### **3. System & Process Management**  
| Command | Description | Example |
|---------|------------|---------|
| `sudo` | Run as superuser | `sudo apt update` |
| `df` | Disk space usage | `df -h` (human-readable) |
| `du` | Directory size | `du -sh folder/` |
| `top` | View running processes | `top` |
| `ps` | List processes | `ps aux` |
| `kill` | Terminate process | `kill -9 PID` |

### **4. Networking Commands**  
| Command | Description | Example |
|---------|------------|---------|
| `ping` | Check connectivity | `ping google.com` |
| `ifconfig` | Network interfaces | `ifconfig` |
| `netstat` | Network stats | `netstat -tuln` |
| `ssh` | Remote login | `ssh user@ip` |
| `wget` | Download files | `wget URL` |

---

## **Advanced Usage**  

### **1. Environment Variables**  
- **View variables**: `echo $PATH`  
- **Set temporarily**: `export VAR=value`  
- **Set permanently**: Add to `~/.bashrc` or `~/.zshrc`  

### **2. File Permissions (`chmod`)**  
- **Read (4)**, **Write (2)**, **Execute (1)**  
- Example:  
  ```bash
  chmod 755 file.txt  # rwx for owner, r-x for group/others
  ```

### **3. Finding Files (`find`, `grep`)**  
- **Find files**:  
  ```bash
  find /path -name "*.txt"  
  find . -type f -size +1M  
  ```
- **Search text (`grep`)**  
  ```bash
  grep "text" file.txt  
  grep -i "text" file.txt  # Case-insensitive  
  ```

### **4. Combining Commands (Pipes & Redirection)**  
| Operator | Description | Example |
|---------|------------|---------|
| `>` | Redirect output | `echo "text" > file.txt` |
| `>>` | Append output | `echo "text" >> file.txt` |
| `|` | Pipe output | `cat file.txt | grep "text"` |
| `&&` | Run if previous succeeds | `cmd1 && cmd2` |
| `||` | Run if previous fails | `cmd1 || cmd2` |

---

## **Tips & Tricks**  
- **Autocomplete**: Press `Tab`  
- **Clear screen**: `clear` or `Ctrl + L`  
- **Command history**: `history`  
- **Run previous command**: `!!`  
- **Kill process**: `Ctrl + C`  
- **Suspend process**: `Ctrl + Z`  
