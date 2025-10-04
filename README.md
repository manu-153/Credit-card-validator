# Credit Card Number Validator (Luhn-Algorithm)

## overview

This C++ program validates credit card numbers using the **Luhn Algorithm**, a simple checksum formula used to validate identification numbers. It helps verify whether a given card number could be valid (used by major credit card companies).

## 🎯 Features

* Accepts user input and checks if it is numeric
* Implements the Luhn algorithm to verify credit card numbers
* Handles invalid input gracefully
* Allows repeated checks in a single run
* Type `'exit'` to quit the program anytime

## 🧠 Luhn Algorithm Summary

1. Starting from the second last digit and moving left, double every second digit.
2. If doubling results in a number greater than 9, subtract 9 from it (or sum the digits).
3. Add all modified digits and the untouched digits from odd positions.
4. If the total sum is divisible by 10,then the number is **valid**.

## 🛠️ How to Compile and Run

### 🔧 Requirements:

* A C++ compiler like `g++`

### ▶️ Compilation:

```bash
g++ credit_card_validator.cpp -o validator
```

### ▶️ Run:

```bash
./validator
```

## 💡 Sample Output

```
This program uses the Luhn Algorithm to validate a credit card number.
You can enter 'exit' anytime to quit.
Please enter a credit card number to validate: 4532015112830366
Valid!
Please enter a credit card number to validate: 1234567890123456
Invalid!
Please enter a credit card number to validate: exit
```

## 🧾 Code Highlights

* **Input Validation:** Ensures only numeric strings are processed
* **Exit Condition:** Type `exit` to quit
* **Modular Design:** Functions split for readability and reuse

## 📂 File Structure

```
📦CreditCardValidator
 ┣ 📄 credit_card_validator.cpp
 ┗ 📄 README.md
```

## 📘 Reference

* [Luhn Algorithm - Wikipedia](https://en.wikipedia.org/wiki/Luhn_algorithm)

