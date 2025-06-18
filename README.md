
# 📚 Multimap Dictionary in C

This project implements a **Multimap Dictionary** — a data structure that maps each unique key to **multiple values**, with both keys and values stored in sorted order.  
It is built using **sorted linked lists** in C.

---

## 📌 Overview

- Each key appears only once.
- Each key can have multiple **sorted** values.
- All operations preserve sort order.
- Great for use cases like contact lists, tag systems, and event logs.

---

## 🧱 Data Structure Design

### 🔹 `ListNode` (Key-Value Node)
- `key`: Integer key  
- `value`: Pointer to `ListValue` (linked list of values)  
- `next`: Pointer to the next `ListNode`

### 🔸 `ListValue` (Value Node)
- `entry`: Integer value  
- `next`: Pointer to the next value in the list

### 🧩 `List` (Multimap Dictionary)
- `head`: Points to the first `ListNode`  
- `size`: Number of unique keys

---

## ⚙️ Supported Operations

- ➕ **Add Pair**: Add a `(key, value)` pair (creates new key if it doesn't exist)  
- ❌ **Remove Key**: Delete a key and all its values  
- 🧹 **Remove Value**: Remove a specific value under a key  
- 📝 **Modify Value**: Replace a value under a key  
- 📄 **Print Values**: Print all values for a given key

---

## 🧪 How to Run

### ✅ Prerequisites
- C Compiler (e.g. `gcc`)  
- Terminal / Command Prompt

### 📥 Clone the Repository

```bash
git clone https://github.com/Reemsoliiman/multimap-dictionary.git
cd multimap-dictionary
````

### 🛠️ Compile the Program

```bash
gcc -o multimap main.c List.c Operation.c Menu.c
```

### ▶️ Run the Program

```bash
./multimap       # For Unix/macOS
multimap.exe     # For Windows
```

---

## 🖱️ Interactive Menu

From the terminal menu, you can:

* Add key-value pairs
* Remove a key or individual value
* Modify specific values
* Print values by key
* Exit the program

> ⚠️ Input must be **positive integers only**

---

## 💡 Example Use Cases

| Use Case           | Description                                                                   |
| ------------------ | ----------------------------------------------------------------------------- |
| 📞 Contact Manager | Store multiple phone numbers for a user ID → e.g., `101 → [1001, 1002, 1003]` |
| 🏷️ Tag System     | Tag IDs to categories → e.g., `1 (Fruits) → [10, 20]`                         |
| 🧾 User Logs       | Track multiple events per user ID → e.g., `5 → [1, 2, 3]`                     |

---

## ⏱️ Time Complexity

| Operation    | Time Complexity |
| ------------ | --------------- |
| Add Pair     | O(n + m)        |
| Remove Key   | O(n)            |
| Remove Value | O(n + m)        |
| Modify Value | O(n + m)        |
| Print Values | O(n + m)        |

Where:

* `n` = number of keys
* `m` = number of values under a key

---

## ✅ Pros

* ✅ Low memory usage
* ✅ Dynamic size
* ✅ Sorted keys and values (no extra sorting needed)

## ⚠️ Cons

* ❌ Slower than hash maps on large data
* ❌ No random access (must traverse)
* ❌ More complex pointer management

---

## 🧠 When to Use

* ✅ Small/medium datasets
* ✅ When sorted output is needed
* ❌ Avoid for high-performance needs (use hash tables or trees instead)

---

## 🚀 Potential Improvements

* 🔍 Better input validation (handle invalid inputs)
* 🧠 Memory allocation checks
* 🔁 Option to allow duplicate values
* 🔤 Support string keys/values
* 💾 Save/load data from files
* ✅ Add unit tests

