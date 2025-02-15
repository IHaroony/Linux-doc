
# **Linux Text Editors: Nano, Vi, and Vim**

## **1. Nano Editor**

Nano is a simple and easy-to-use text editor for Linux, perfect for beginners.

### **Opening a File in Nano**

```
nano filename.txt
```

- If the file does not exist, Nano will create it.
    

### **Basic Navigation**

- **Arrow Keys**: Move cursor up, down, left, and right.
    
- **Ctrl + A**: Move to the beginning of the line.
    
- **Ctrl + E**: Move to the end of the line.
    
- **Ctrl + Y**: Scroll up a page.
    
- **Ctrl + V**: Scroll down a page.
    

### **Editing and Saving**

- **Type normally to enter text.**
    
- **Ctrl + K**: Cut the entire line.
    
- **Ctrl + U**: Paste the cut line.
    
- **Ctrl + O**: Save the file (press **Enter** to confirm).
    
- **Ctrl + X**: Exit Nano (press **Y** to save if needed).
    

---

## **2. Vi Editor**

Vi is a traditional text editor found on most Linux systems. It has two main modes:

- **Command Mode** (default): Used for navigation and commands.
    
- **Insert Mode**: Used for text editing.
    

### **Opening a File in Vi**

```
vi filename.txt
```

### **Switching to Insert Mode**

- Press **i** to enter **Insert Mode**.
    
- Start typing to edit the file.
    

### **Navigating in Vi (Command Mode)**

- **h**: Move left.
    
- **l**: Move right.
    
- **j**: Move down.
    
- **k**: Move up.
    
- **0**: Move to the beginning of the line.
    
- **$**: Move to the end of the line.
    
- **G**: Move to the end of the file.
    
- **gg**: Move to the beginning of the file.
    
- **Ctrl + d**: Scroll down half a page.
    
- **Ctrl + u**: Scroll up half a page.
    

### **Saving and Exiting Vi**

- Press **Esc** to switch to **Command Mode**.
    
- Type `:w` and press **Enter** to save.
    
- Type `:q` and press **Enter** to exit.
    
- Type `:wq` and press **Enter** to save and exit.
    
- Type `:q!` and press **Enter** to exit without saving.
    

---

## **3. Vim Editor (Vi Improved)**

Vim is an improved version of Vi with additional features like syntax highlighting and undo history.

### **Opening a File in Vim**

```
vim filename.txt
```

### **Navigation (Same as Vi)**

- **h, j, k, l**: Move left, down, up, right.
    
- **gg**: Go to the beginning of the file.
    
- **G**: Go to the end of the file.
    
- **Ctrl + d**: Scroll down.
    
- **Ctrl + u**: Scroll up.
    

### **Editing in Vim**

- Press **i** to enter Insert Mode.
    
- Press **Esc** to exit Insert Mode.
    
- Press **u** to undo.
    
- Press **Ctrl + r** to redo.
    

### **Saving and Exiting Vim**

- `:w` → Save the file.
    
- `:q` → Exit Vim.
    
- `:wq` → Save and exit.
    
- `:q!` → Exit without saving.
    

---

## **Comparison Table**

|Feature|Nano|Vi|Vim|
|---|---|---|---|
|Beginner-friendly|✅|❌|❌|
|Default on Linux|✅|✅|✅|
|Syntax Highlighting|❌|❌|✅|
|Undo Feature|✅|❌|✅|
|Multi-file Editing|❌|✅|✅|

---

## **Conclusion**

- Use **Nano** if you are a beginner and want a simple editor.
    
- Use **Vi** if you are working on minimal Linux environments.
    
- Use **Vim** if you need powerful text editing features.
    

Want to practice? Try running:

```
nano test.txt
vi test.txt
vim test.txt
```

Experiment with different commands and see what works best for you!