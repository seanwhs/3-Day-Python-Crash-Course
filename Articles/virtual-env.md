# `py -m venv venv` vs `virtualenv venv`

## Executive Summary

| Aspect                    | `py -m venv venv`          | `virtualenv venv`                   |
| ------------------------- | -------------------------- | ----------------------------------- |
| Comes with Python         | ✅ Yes (stdlib)             | ❌ No (3rd-party)                    |
| Needs install             | ❌ No                       | ✅ `pip install virtualenv`          |
| Python version used       | Current Python interpreter | Any Python you specify              |
| Speed                     | Normal                     | ⚡ Faster (especially older Pythons) |
| Cross-version support     | Limited                    | Excellent                           |
| Most common today         | ✅ Yes                      | Still widely used                   |
| Recommended for beginners | ✅ Strongly                 | ⚠️ Maybe later                      |

---

## 1️⃣ `py -m venv venv` (Built-in Standard Library)

### What it is

* Uses Python’s **built-in `venv` module**
* Ships with Python **3.3+**
* No external dependencies

### Command

```bash
py -m venv venv
```

On macOS / Linux:

```bash
python3 -m venv venv
```

### What happens internally

* Copies (or symlinks) the Python interpreter
* Creates:

  ```
  venv/
    Scripts/ (Windows) or bin/ (macOS/Linux)
    Lib/
    pyvenv.cfg
  ```
* Uses the **same Python version** you ran the command with

### Activation

```bash
# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

### Strengths

✅ Official
✅ Simple
✅ Zero setup
✅ Perfect for **learning, labs, training, CI**

### Limitations

❌ Cannot easily create venvs for **other Python versions**
❌ Slower creation (minor, but noticeable in large CI setups)

---

### Trainer Explanation (Mental Model)

> “`venv` is Python’s **official sandbox** — simple, predictable, and good enough for 90% of use cases.”

---

## 2️⃣ `virtualenv venv` (Third-Party Power Tool)

### What it is

* A **third-party package** that existed *before* `venv`
* Still maintained and widely used
* Adds **advanced features**

### Install

```bash
pip install virtualenv
```

### Create environment

```bash
virtualenv venv
```

Specify Python version:

```bash
virtualenv -p python3.11 venv
```

### What it does differently

* Can create environments for:

  * Older Python versions
  * Multiple Python installs
* Faster environment creation
* More configuration options

---

### Strengths

✅ Works with **many Python versions**
✅ Faster creation
✅ More flexible
✅ Excellent for **multi-Python testing**

### Limitations

❌ Extra dependency
❌ Slightly more complex
❌ Overkill for beginners

---

### Trainer Explanation (Mental Model)

> “`virtualenv` is a **power drill** — more features, faster, but you need to know what you’re doing.”

---

## 3️⃣ Key Technical Differences (Under the Hood)

### Interpreter Selection

```bash
py -m venv venv
```

➡️ Uses the Python running the command

```bash
virtualenv -p python3.9 venv
```

➡️ Uses explicitly selected interpreter

---

### Bootstrapping `pip`

| Feature      | venv      | virtualenv |
| ------------ | --------- | ---------- |
| pip included | Sometimes | Always     |
| setuptools   | Sometimes | Always     |
| wheel        | Sometimes | Always     |

---

### Performance (CI/CD Insight)

* `virtualenv` caches wheels → faster repeated creation
* `venv` recreates everything each time

This is why **GitHub Actions** and **tox** often use `virtualenv`.

---

## 4️⃣ When Should You Use Which?

### ✅ Use `py -m venv` when:

* Teaching Python
* Running workshops or labs
* Working on a single project
* Using modern Python (3.9+)
* You want **zero setup friction**

👉 **Best default choice**

---

### ✅ Use `virtualenv` when:

* Testing across Python versions
* Maintaining legacy code
* Building CI/CD pipelines
* Need performance and flexibility

---

## 5️⃣ Real-World Trainer Recommendation

### For your Python Crash Course:

```bash
py -m venv venv
```

**Why?**

* Students already struggle with environment setup
* Built-in tool = fewer things to go wrong
* Works everywhere Python is installed

---

### For advanced or professional modules:

Introduce:

* `virtualenv`
* `pyenv`
* `pipenv`
* `poetry`

---

## 6️⃣ Common Student Pitfalls (Important!)

❌ Forgetting to activate the venv
❌ Installing packages globally
❌ Creating venv with Python 3.12 but running with Python 3.9
❌ Confusing `pip` vs `pip3` vs `python -m pip`

---

### Best Practice (Teach This!)

```bash
python -m pip install package_name
```

Why?

* Guarantees pip belongs to the active interpreter

---

## 7️⃣ Final One-Sentence Summary

> **`py -m venv` is the official, simple, built-in solution — `virtualenv` is a faster, more flexible, power-user tool.**

---


Just tell me 👍
