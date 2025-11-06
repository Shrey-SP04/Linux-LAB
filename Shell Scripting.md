 # 🐚 Shell Scripting Tutorial!!

Shell scripting allows you to **automate tasks** in Linux/Unix by writing commands inside a file that the shell executes line by line.

---

## 1. 🔹 What is a Shell Script?

* A **shell** is a command-line interpreter (e.g., `bash`, `zsh`, `sh`).
* A **shell script** is a text file with a series of commands.
* File usually has **`.sh`** extension, though not mandatory.

**Example: `hello.sh`**

```bash
#!/bin/bash
echo "Hello, World!"
```
<img width="560" height="72" alt="image" src="https://github.com/user-attachments/assets/70b56e55-eea1-4ef3-983c-cd314aa98557" />

Run it:

```bash
chmod +x hello.sh   # make it executable
./hello.sh
```

Output:

```
Hello, World!
```
<img width="572" height="158" alt="image" src="https://github.com/user-attachments/assets/6ae0f477-be53-4ae2-8e14-8f421613537a" />

---

## 2. 🔹 Variables

Variables store data (text, numbers, paths, etc.).

### Defining variables

```bash
name="Rishabh Negi"
age=18
```

⚠️ No spaces around `=`.

### Accessing variables

```bash
echo "My name is $name and I am $age years old."
```

Output:

```
My name is Shreyas Parida and I am 18 years old.
```
### Environment variables

```bash
echo $HOME   # home directory
echo $USER   # current user
echo $PWD    # present working directory
```

---

## 3. 🔹 User Input

Read input from user with `read`.

```bash
#!/bin/bash
echo "Enter your favorite language:"
read lang
echo "You chose $lang"
```
<img width="590" height="116" alt="image" src="https://github.com/user-attachments/assets/ff9a8497-6626-4684-b9f0-f925b6eb6e65" />

---

## 4. 🔹 Conditional Statements (if-else)

```bash
#!/bin/bash
num=10

if [ $num -gt 5 ]; then
    echo "Number is greater than 5"
else
    echo "Number is less than or equal to 5"
fi
```
<img width="587" height="61" alt="image" src="https://github.com/user-attachments/assets/13690599-f286-449d-8513-271ed600db23" />

Operators:

* `-eq` (equal)
* `-ne` (not equal)
* `-gt` (greater than)
* `-lt` (less than)
* `-ge` (greater or equal)
* `-le` (less or equal)

---

## 5. 🔹 Loops

### For loop

```bash
for i in 1 2 3 4 5
do
    echo "Number: $i"
done
```

Or use a range:

```bash
for i in {1..5}
do
    echo "Iteration $i"
done
```

### While loop

```bash
count=1
while [ $count -le 5 ]
do
    echo "Count: $count"
    ((count++))   # increment
done
```

### Until loop

Runs until condition becomes true.

```bash
x=1
until [ $x -gt 5 ]
do
    echo "Value: $x"
    ((x++))
done
```

---

## 6. 🔹 Functions

Encapsulate reusable code.

```bash
greet() {
    echo "Hello, $1"
}

greet Shreyas
greet World
```
<img width="236" height="111" alt="image" src="https://github.com/user-attachments/assets/04f2ffe1-af74-460e-a7ed-600426638240" />

Output:

```
Hello, Shreyas
Hello, World
```
<img width="504" height="71" alt="image" src="https://github.com/user-attachments/assets/abeb33c8-d03e-48e6-a5bc-af6944a717d5" />


---

## 7. 🔹 Command Line Arguments

Access arguments passed to script:

```bash
#!/bin/bash
echo "Script name: $0"
echo "First argument: $1"
echo "Second argument: $2"
echo "All arguments: $@"
echo "Number of arguments: $#"
```

Run:

```bash
./script.sh apple banana
```

Output:

```
Script name: ./script.sh
First argument: apple
Second argument: banana
All arguments: apple banana
Number of arguments: 2
```
<img width="615" height="162" alt="image" src="https://github.com/user-attachments/assets/b24a69e0-c4ae-4992-876e-f038b6f811dd" />

---

## 8. 🔹 Arrays

```bash
fruits=("apple" "banana" "cherry")

echo "First fruit: ${fruits[0]}"

for fruit in "${fruits[@]}"; do
    echo "Fruit: $fruit"
done
```

---

## 9. 🔹 Useful Commands in Scripts

* `date` → show current date/time
* `whoami` → show current user
* `ls` → list files
* `pwd` → print working directory
* `cat` → read file contents

---

## 10. 🔹 A Practical Example

**Backup script (`backup.sh`):**

```bash
#!/bin/bash
# Backup home directory to /tmp

backup_file="/tmp/home_backup_$(date +%Y%m%d%H%M%S).tar.gz"

tar -czf $backup_file $HOME

echo "Backup saved to $backup_file"
```

Run:

```bash
./backup.sh
```

---

## 📚 Summary

| 🔑 Concept   | 📜 Example         |
| ------------ | ------------------ |
| Script       | `./hello.sh`       |
| Variables    | `name="Mudit"`     |
| Input        | `read var`         |
| Conditionals | `if [ $a -gt 5 ]`  |
| Loops        | `for i in {1..5}`  |
| Functions    | `greet() { ... }`  |
| Args         | `$0 $1 $2 $@ $#`   |
| Arrays       | `fruits=("a" "b")` |
| Backup       | `tar -czf`         |

---

💡 **Pro Tip:** Shell scripting = 💪 Power + ⚡ Automation + 🚀 Productivity.
Keep practicing by writing **small utility scripts** to master it!

```

```
![Screenshot of A3](A3.png)
![Screenshot of A3](A3.png)
