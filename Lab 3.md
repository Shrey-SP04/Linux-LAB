# 📝 **Assignment 3 – Modify an Existing Script**


Name-Shreyas Parida

sap id-590026387

## 🎯 **Objective**
> Enhance and customize a script by adding user input and validation.

## 🚦 **Tasks Overview**
- Select a script from `Scripts/` 
- Modify it so the user provides start, end, and step values as input
- Validate inputs (e.g., step must be positive)
- Save as `enhanced_numbers.sh`
- Explain original vs. new behavior and show example

- 
![WhatsApp Image 2025-11-06 at 10 48 55_3ff7bfae](https://github.com/user-attachments/assets/6dde48fe-33f5-4ead-ad5e-c54d1a31ef5d)


![WhatsApp Image 2025-11-06 at 10 49 42_7e3eed7c](https://github.com/user-attachments/assets/617771de-4a34-4eeb-9278-b7009129f93d)



## **🔄Question -Original vs. Enhanced Behavior**
1. Input Handling

Original: Numbers 1 2 3 4 5 are fixed inside the script. User cannot change them without editing the code.

New: User is asked to enter start, end, and step values directly when running the script.

2. Flexibility

Original: Always prints the same sequence 1 → 5 with step 1.

New: Can print any sequence (e.g., 2 4 6 8 10 or 5 10 15) depending on user’s input, making it more customizable.

3. Validation

Original: No validation at all. The loop just runs as written.

New: Validates the step value to ensure it’s positive. If the user enters 0 or a negative number, the script shows an error and stops.

## ▶️ Question - Example run with different inputs.

![WhatsApp Image 2025-11-06 at 10 49 55_d29a29d7](https://github.com/user-attachments/assets/f2b943cd-d93c-46d9-a118-52e8a515f307)


## ❓ **Extra Questions**

### 1️⃣ What is the difference between `$1`, `$@`, and `$#` in bash?

$1 → Refers to the first argument passed to the script.

$@ → Represents all arguments passed to the script as separate words.

$# → Gives the total number of arguments passed to the script.

### 2️⃣ What does `exit 1` mean in a script?

exit stops the script immediately.
The number after exit is the exit status ,
0 → Success
Non-zero (like 1) → Indicates an error or failure
In your script, exit 1 is used when the user enters an invalid step (=< 0) to stop execution and signal an error.
