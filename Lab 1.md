# 📝 **Assignment 1 – Unit-1: Linux Basics**

---



Name-Shreyas Parida

sap id-590026387


Here's a **detailed tutorial on basic terminal commands** that work on **Linux, macOS, and Git Bash (Windows)**. These commands are essential for navigating and managing files from the terminal, especially for coding and version control (e.g., Git, VS Code, etc.).

---

## ✅ 1. **Navigation Commands**

### `pwd` – Print Working Directory

Shows the current location in the filesystem.

```bash
pwd
```


📌 Output example:

```
/Users/yourname/projects
```
<img width="343" height="43" alt="image" src="https://github.com/user-attachments/assets/034924eb-6f67-42ef-bdad-ab2d0412c3c3" />

---

### `ls` – List Directory Contents

Lists files and folders in the current directory.

```bash
ls
```

* `ls -l` → Detailed list (permissions, size, date)
* `ls -a` → Shows hidden files (those starting with `.`)
* `ls -la` → Combined

---
<img width="358" height="44" alt="image" src="https://github.com/user-attachments/assets/2dfe44e4-8e77-405c-bf71-dc0e189ce27b" />


### `cd` – Change Directory

Moves into a directory.

```bash
cd folder_name
```

<img width="456" height="48" alt="image" src="https://github.com/user-attachments/assets/d50a78d3-b53e-4605-85fd-705304b68289" />

Examples:

```bash
cd Documents        # Go to Documents
cd ..               # Go up one level
cd /                # Go to root
cd ~                # Go to home directory
```

---

## ✅ 2. **File and Directory Management**

### `mkdir` – Make Directory

Creates a new folder.

```bash
mkdir new_folder
```
<img width="456" height="48" alt="image" src="https://github.com/user-attachments/assets/1ec2653f-5e6f-4af2-a870-bc2482742592" />


---

### `touch` – Create File

Creates an empty file.

```bash
touch file.txt
```
<img width="720" height="27" alt="image" src="https://github.com/user-attachments/assets/7b526634-c716-46fe-8f4a-7c88f4c86000" />

---

### `cp` – Copy Files or Directories

```bash
cp source.txt destination.txt
```
<img width="824" height="26" alt="image" src="https://github.com/user-attachments/assets/307af9a4-13d3-4d05-8555-bac2f9cfa067" />

* Copy folder:

```bash
cp -r folder1 folder2
```
<img width="824" height="55" alt="image" src="https://github.com/user-attachments/assets/984a7b64-a64a-4aae-8c24-cd929d76d1a6" />

---

### `mv` – Move or Rename Files

```bash
mv oldname.txt newname.txt
```

```bash
mv file.txt ~/Documents/     # Move file
```

---

### `rm` – Remove Files

```bash
rm file.txt          # Delete file
rm -r folder_name    # Delete folder (recursively)
```
<img width="695" height="22" alt="image" src="https://github.com/user-attachments/assets/721cab3c-2e08-4cfe-9273-3b5d7d9e45e3" />


⚠️ **Be careful!** There is no undo.

---

## ✅ 3. **File Viewing & Editing**

### `cat` – View File Contents

Displays content in terminal.

```bash
cat file.txt
```

---

### `nano` – Edit Files in Terminal

A basic terminal-based text editor.

```bash
nano file.txt
```

* Use arrows to move
* `CTRL + O` to save
* `CTRL + X` to exit

---
<img width="439" height="16" alt="image" src="https://github.com/user-attachments/assets/ec90c76c-b9a2-491c-967a-3a185f3d39f5" />
<img width="813" height="535" alt="image" src="https://github.com/user-attachments/assets/28d0691d-811d-4735-a334-e28e55b88132" />


### `clear` – Clears the Terminal

```bash
clear
```

Shortcut: `CTRL + L`
<img width="544" height="96" alt="image" src="https://github.com/user-attachments/assets/93112681-d159-4c27-9e91-a455e66b04a4" />

---

## ✅ 4. **System Commands**

### `echo` – Print Text

Useful for debugging or scripting.

```bash
echo "Hello, World!"
```
<img width="623" height="44" alt="image" src="https://github.com/user-attachments/assets/2f8bfd28-9afa-4503-8ccf-dd29f899cacf" />


---

### `whoami` – Show Current User

```bash
whoami
```
<img width="542" height="43" alt="image" src="https://github.com/user-attachments/assets/85bf1deb-d9c3-442b-9d2c-ae872d7adff6" />


---

### `man` – Manual for Any Command

```bash
man ls
```

Use `q` to quit the manual.

---

## ✅ 5. **Searching and Finding**

### `find` – Locate Files

```bash
find . -name "*.txt"
```

🔍 Finds all `.txt` files in current folder and subfolders.

---

### `grep` – Search Inside Files

```bash
grep "hello" file.txt
```

🔍 Searches for the word `hello` inside `file.txt`.


---

## ✅ 6. **Helpful Shortcuts**

| Shortcut   | Action                      |
| ---------- | --------------------------- |
| `Tab`      | Auto-complete files/folders |
| `↑ / ↓`    | Browse command history      |
| `CTRL + C` | Stop a running command      |
| `CTRL + L` | Clear screen                |

---

## ✅ 7. **Bonus: Chaining Commands**

* **Run multiple commands**:

```bash
mkdir test && cd test && touch hello.txt
```

* **Run only if previous command succeeds**: `&&`
* **Run regardless of success**: `;`

---

// What is differece b\w chmod and chown?
=>chmod     

  changes permissions of a file or directory.                                     
  decides whether a user can read, write, or execute a file.                            
  affects access rights.                                                                 

=>chown

  changes the ownership of a file or directory.
  decides which user or group owns the file.
  chown affects file ownership.
