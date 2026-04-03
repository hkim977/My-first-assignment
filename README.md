
hkim9771852@c4r5s1 ~ % pwd
/Users/hkim9771852
hkim9771852@c4r5s1 ~ % ls -la
total 16
drwxr-x---+ 20 hkim9771852  hkim9771852   640 Apr  3 18:55 .
drwxr-xr-x  11 root         admin         352 Apr  3 18:15 ..
-r--------   1 hkim9771852  hkim9771852     7 Apr  3 18:15 .CFUserTextEncoding
drwx------+  2 hkim9771852  hkim9771852    64 Apr  3 18:16 .Trash
drwxr-xr-x   5 hkim9771852  hkim9771852   160 Apr  3 18:16 .docker
drwxr-xr-x  10 hkim9771852  hkim9771852   320 Apr  3 18:55 .orbstack
drwxr-xr-x   3 hkim9771852  hkim9771852    96 Apr  3 18:16 .ssh
drwxr-xr-x   3 hkim9771852  hkim9771852    96 Apr  3 18:16 .vscode
-rw-------   1 hkim9771852  hkim9771852    44 Apr  3 18:54 .zsh_history
drwx------   6 hkim9771852  hkim9771852   192 Apr  3 18:55 .zsh_sessions
drwx------@  4 hkim9771852  hkim9771852   128 Apr  3 18:44 Applications
drwx------+  3 hkim9771852  hkim9771852    96 Apr  3 18:15 Desktop
drwx------+  3 hkim9771852  hkim9771852    96 Apr  3 18:15 Documents
drwx------+  3 hkim9771852  hkim9771852    96 Apr  3 18:15 Downloads
drwx------@ 80 hkim9771852  hkim9771852  2560 Apr  3 18:39 Library
drwx------   3 hkim9771852  hkim9771852    96 Apr  3 18:15 Movies
drwx------+  3 hkim9771852  hkim9771852    96 Apr  3 18:15 Music
drwx------   4 hkim9771852  hkim9771852   160 Apr  3 18:55 OrbStack
drwx------+  4 hkim9771852  hkim9771852   128 Apr  3 18:16 Pictures
drwxr-xr-x+  4 hkim9771852  hkim9771852   128 Apr  3 18:15 Public
hkim9771852@c4r5s1 ~ % mkdir dictation
hkim9771852@c4r5s1 ~ % cd dictation
hkim9771852@c4r5s1 dictation % touch Baking.txt
hkim9771852@c4r5s1 dictation % echo "Hello" > Baking.txt
hkim9771852@c4r5s1 dictation % cat Baking.txt
Hello
hkim9771852@c4r5s1 dictation % cp Baking.txt Baking-copy.txt
hkim9771852@c4r5s1 dictation % mv Baking-copy.txt Baking-renamed.txt
hkim9771852@c4r5s1 dictation % rm Baking-renamed.txt
hkim9771852@c4r5s1 dictation % ls -la
total 8
drwxr-xr-x   3 hkim9771852  hkim9771852   96 Apr  3 19:30 .
drwxr-x---+ 21 hkim9771852  hkim9771852  672 Apr  3 19:24 ..
-rw-r--r--   1 hkim9771852  hkim9771852    6 Apr  3 19:25 Baking.txt

With comments:
# 📁 Basic File Operations in macOS Terminal

This document demonstrates fundamental file and directory operations using the macOS terminal. Each command is accompanied by a brief explanation.

---

## 1. Check Current Directory

```bash
pwd
```

**Description:**
Prints the current working directory.

**Output:**

```
/Users/hkim9771852
```

---

## 2. List Directory Contents

```bash
ls -la
```

**Description:**
Lists all files and directories (including hidden ones) in long format, showing permissions, ownership, size, and timestamps.

---

## 3. Create a New Directory

```bash
mkdir dictation
```

**Description:**
Creates a new directory named `dictation`.

---

## 4. Navigate into Directory

```bash
cd dictation
```

**Description:**
Changes the current working directory to `dictation`.

---

## 5. Create a New File

```bash
touch Baking.txt
```

**Description:**
Creates an empty file named `Baking.txt`.

---

## 6. Write Content to File

```bash
echo "Hello" > Baking.txt
```

**Description:**
Writes the text `"Hello"` into `Baking.txt`.

* If the file already exists, it will be overwritten.

---

## 7. Display File Contents

```bash
cat Baking.txt
```

**Description:**
Displays the contents of `Baking.txt`.

**Output:**

```
Hello
```

---

## 8. Copy a File

```bash
cp Baking.txt Baking-copy.txt
```

**Description:**
Creates a copy of `Baking.txt` named `Baking-copy.txt`.

---

## 9. Rename a File

```bash
mv Baking-copy.txt Baking-renamed.txt
```

**Description:**
Renames `Baking-copy.txt` to `Baking-renamed.txt`.

---

## 10. Delete a File

```bash
rm Baking-renamed.txt
```

**Description:**
Deletes the file `Baking-renamed.txt`.

---

## 11. Verify Final Directory Contents

```bash
ls -la
```

**Description:**
Confirms the remaining files in the directory.

**Result:**
Only `Baking.txt` remains.

---

## ✅ Summary

This exercise covers:

* Directory navigation (`pwd`, `cd`)
* File and directory management (`mkdir`, `touch`, `cp`, `mv`, `rm`)
* File content manipulation (`echo`, `cat`)
* File inspection (`ls -la`)

These commands form the foundation of working efficiently in a Unix-based terminal environment.

---
