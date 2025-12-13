--------------------------------------------------------
PYTHON CRASH COURSE – SEAN WONG 2025
--------------------------------------------------------
Module 1  Foundation  
Module 2  Intermediate  
Module 3  Advanced  
Appendix  Tooling & Eco-system
--------------------------------------------------------

========================================================
Module 1  FOUNDATION
========================================================
Slide 1  Why Python?
--------------------------------------------------------
• Readable, indentation-driven syntax  
• Huge standard library (“batteries included”)  
• Cross-platform, open-source, massive community  
• Runs servers, scripts, science, games, IoT, Excel…

--------------------------------------------------------
Slide 2  Installing & Running
--------------------------------------------------------
# 1. Official installer (Windows/macOS)
https://www.python.org/downloads/

# 2. Linux package manager
sudo apt update && sudo apt install python3 python3-venv

# 3. Verify
python3 -V              # ≥ 3.9 recommended
python3 -m pip --version

# 4. REPL quick start
>>> 2 + 2
4
>>> print("Hello", "world", sep=" 🐍 ")
Hello 🐍 world

--------------------------------------------------------
Slide 3  Variables & Dynamic Typing
--------------------------------------------------------
# No declarations
age = 25                # int
price = 19.99           # float
name = "Monty"          # str
found = True            # bool

# Re-assign freely (dynamic)
age = "twenty-five"     # now str
# ^-- the variable label simply moves to a new object

# id() shows memory address
x = 10
print(id(x))            # 140735…
x = x + 1               # new int object, id changes!

--------------------------------------------------------
Slide 4  Core Built-in Types (quick reference)
--------------------------------------------------------
int        0  -42  1_000_000
float      0.0  3.14159  6.02e23
complex    3+4j
str        'spam'  "spam"  """multi-line"""
bool       True  False
NoneType   None               # singleton “nothing”

--------------------------------------------------------
Slide 5  Numbers & Operators
--------------------------------------------------------
# Division behavior
7 / 3            # 2.333…  (float)
7 // 3           # 2       (floor int)
7 % 3            # 1       (modulo)
divmod(7, 3)     # (2, 1)  tuple pair

# Power & roots
2 ** 10          # 1024
pow(2, 10, 100)  # 24  (modular exponentiation)

# Decimal for money
from decimal import Decimal
price = Decimal('19.99')
tax   = price * Decimal('0.07')   # exact, no binary error

--------------------------------------------------------
Slide 6  Strings – indexing, slicing, methods
--------------------------------------------------------
s = "Python"
s[0]            # 'P'        (0-based)
s[-1]           # 'n'        (negative index)
s[1:4]          # 'yth'      (slice: start ≤ i < stop)
s[::-1]         # 'nohtyP'   (reverse)

# Immutability
s[0] = 'J'      # TypeError

# Common methods
"hello".upper()                 # 'HELLO'
"  spaced  ".strip()            # 'spaced'
"cat,dog,bird".split(",")       # ['cat', 'dog', 'bird']
"-".join(["A", "B", "C"])       # 'A-B-C'

# f-strings (fast, readable)
name, age = "Ada", 36
f"{name=} is {age=}"            # name='Ada' is age=36

--------------------------------------------------------
Slide 7  Booleans & Truthiness
--------------------------------------------------------
# Explicit
is_valid = True

# Implicit (falsy values)
0  0.0  ""  []  {}  None  set()

# Quick filter
users = ["", "Ada", "", "Linus"]
real_users = [u for u in users if u]   # ['Ada', 'Linus']

--------------------------------------------------------
Slide 8  Type Casting & Input
--------------------------------------------------------
# Safe casting with default
def to_int(text, default=None):
    try:
        return int(text)
    except ValueError:
        return default

# Command-line input
birth = input("Birth year: ")
age = 2025 - int(birth)
print(f"You turn {age} this year")

--------------------------------------------------------
Slide 9  Control Flow – if / elif / else
--------------------------------------------------------
# Loan eligibility – verbose version
income = 58_000
credit = 720
debt_ratio = 0.28

if income > 50_000:
    if credit > 700:
        if debt_ratio < 0.3:
            print("✅ Approved")
        else:
            print("❌ Debt ratio too high")
    else:
        print("❌ Credit score low")
else:
    print("❌ Income insufficient")

# Flatten with and
if income > 50_000 and credit > 700 and debt_ratio < 0.3:
    print("✅ Approved")
else:
    print("❌ Rejected")

--------------------------------------------------------
Slide 10  Ternary Expression
--------------------------------------------------------
status = "Approved" if score > 700 else "Denied"
# Chained
tier = "High" if income > 100_000 else "Mid" if income > 50_000 else "Low"

--------------------------------------------------------
Slide 11  Loops – for & while
--------------------------------------------------------
# for with range
for i in range(5):          # 0 1 2 3 4
    print(i, end=" ")
print()

# Iterating collections
colors = ["red", "green", "blue"]
for color in colors:
    print(color.upper())

# Enumerate gives index
for idx, color in enumerate(colors, start=1):
    print(f"{idx}. {color}")

# while with else
n = 5
while n > 0:
    print(n)
    n -= 1
else:
    print("Blast off!")

--------------------------------------------------------
Slide 12  Break, Continue, Else
--------------------------------------------------------
# Find first prime in list
nums = [10, 15, 18, 19, 20]
for n in nums:
    if n % 2 == 0:
        continue
    for i in range(3, int(n**0.5)+1, 2):
        if n % i == 0:
            break
    else:                       # no break → prime
        print("Prime:", n)
        break                   # stop search
else:
    print("No prime found")

--------------------------------------------------------
Slide 13  Functions – the basics
--------------------------------------------------------
def greet(name="stranger"):
    """Return a greeting."""
    return f"Hello, {name}!"

print(greet())          # Hello, stranger!
print(greet("Ada"))     # Hello, Ada!

# Docstring appears in help
help(greet)

--------------------------------------------------------
Slide 14  Multiple Returns
--------------------------------------------------------
def divide(a, b):
    """Return (quotient, remainder)."""
    return a // b, a % b

q, r = divide(20, 3)
print(q, r)             # 6 2

--------------------------------------------------------
Slide 15  *args  **kwargs
--------------------------------------------------------
def log(message, *args, **kwargs):
    print(f"[LOG] {message}")
    if args:
        print("  Extra positional:", args)
    if kwargs:
        print("  Extra keyword:", kwargs)

log("Start", 1, 2, 3, user="Ada", code=42)

--------------------------------------------------------
Slide 16  Lambda & Sorted
--------------------------------------------------------
pairs = [(1, "one"), (2, "two"), (3, "three")]
pairs.sort(key=lambda x: x[1])   # sort by string
print(pairs)                     # [(1, 'one'), (3, 'three'), (2, 'two')]

--------------------------------------------------------
Slide 17  Mini-Project: CLI Calculator
--------------------------------------------------------
"""
calc.py – run with:  python calc.py 3 + 4
"""
import sys

ops = {
    "+": lambda x, y: x + y,
    "-": lambda x, y: x - y,
    "*": lambda x, y: x * y,
    "/": lambda x, y: x / y,
}

if len(sys.argv) != 4:
    print("Usage: calc.py <num> <op> <num>")
    sys.exit(1)

_, a, op, b = sys.argv
try:
    result = ops[op](float(a), float(b))
    print(result)
except KeyError:
    print("Unsupported op")
except ZeroDivisionError:
    print("Cannot divide by zero")

========================================================
Module 2  INTERMEDIATE
========================================================
Slide 18  Object-Oriented Programming – Classes
--------------------------------------------------------
class Dog:
    """A simple dog object."""

    species = "Canis familiaris"   # class variable

    def __init__(self, name, age):
        self.name = name           # instance variable
        self.age = age

    def __str__(self):
        return f"{self.name} is {self.age} years old"

    def speak(self, sound="Woof!"):
        return f"{self.name} says {sound}"

# Usage
d = Dog("Buddy", 4)
print(d)                    # Buddy is 4 years old
print(d.speak("Ruff"))      # Buddy says Ruff

--------------------------------------------------------
Slide 19  Encapsulation & “Private” Attributes
--------------------------------------------------------
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.__balance = balance      # name mangled

    def deposit(self, amount):
        if amount <= 0:
            raise ValueError("Positive amount required")
        self.__balance += amount

    def apply_fee(self, fee=5):
        self.__balance -= fee

    @property
    def balance(self):
        return self.__balance

acct = BankAccount("Ada")
acct.deposit(100)
print(acct.balance)         # 100
# acct.__balance            # AttributeError

--------------------------------------------------------
Slide 20  Inheritance & Polymorphism
--------------------------------------------------------
class Animal:
    def speak(self):
        raise NotImplementedError

class Cat(Animal):
    def speak(self):
        return "Meow"

class Cow(Animal):
    def speak(self):
        return "Moo"

def animal_sound(animal: Animal):
    print(animal.speak())

for creature in [Cat(), Cow()]:
    animal_sound(creature)

--------------------------------------------------------
Slide 21  super() & Cooperative Multiple Inheritance
--------------------------------------------------------
class Person:
    def __init__(self, name):
        self.name = name

class Employee(Person):
    def __init__(self, name, salary):
        super().__init__(name)
        self.salary = salary

class Manager(Employee):
    def __init__(self, name, salary, level):
        super().__init__(name, salary)
        self.level = level

m = Manager("Grace", 120_000, "L3")
print(m.name, m.salary, m.level)

--------------------------------------------------------
Slide 22  Dunder (Magic) Methods
--------------------------------------------------------
class Vector:
    def __init__(self, x, y):
        self.x, self.y = x, y

    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)

    def __mul__(self, scalar):
        return Vector(self.x * scalar, self.y * scalar)

    def __repr__(self):
        return f"Vector({self.x}, {self.y})"

v1 = Vector(2, 3)
v2 = Vector(1, 4)
print(v1 + v2)              # Vector(3, 7)
print(v1 * 3)               # Vector(6, 9)

--------------------------------------------------------
Slide 23  Modules – Creating & Importing
--------------------------------------------------------
# project/
#   ├── geometry/
#   │   ├── __init__.py
#   │   └── shapes.py
#   └── app.py

# shapes.py
def area_circle(r):
    from math import pi
    return pi * r ** 2

# __init__.py
from .shapes import area_circle
__all__ = ["area_circle"]

# app.py
from geometry import area_circle
print(area_circle(5))

--------------------------------------------------------
Slide 24  Import Patterns & Aliases
--------------------------------------------------------
import datetime as dt
from pathlib import Path
from collections import defaultdict, Counter

# Wildcard (use sparingly)
from math import *             # pollutes namespace
print(sqrt(2))                 # works but risky

--------------------------------------------------------
Slide 25  File I/O – Text & CSV
--------------------------------------------------------
# Write text
with open(" haiku.txt", "w", encoding="utf-8") as f:
    f.write("Ancient silent pond\n")
    f.write("A frog jumps into the pond—\n")
    f.write("Splash! Silence again.\n")

# Read line by line
with open("haiku.txt") as f:
    for lineno, line in enumerate(f, 1):
        print(f"{lineno}: {line.rstrip()}")

# CSV dictionary
import csv
rows = [
    {"name": "Ada",  "age": 36},
    {"name": "Linus", "age": 52},
]
with open("users.csv", "w", newline="") as f:
    writer = csv.DictWriter(f, fieldnames=["name", "age"])
    writer.writeheader()
    writer.writerows(rows)

--------------------------------------------------------
Slide 26  pathlib vs os.path
--------------------------------------------------------
from pathlib import Path

root = Path("docs") / "letters"   # operator overload
for file in root.glob("*.txt"):
    print(file.stem)              # filename without suffix

--------------------------------------------------------
Slide 27  JSON Serialization
--------------------------------------------------------
import json
data = {"name": "Ada", "skills": ["Python", "Math"]}
with open("ada.json", "w") as f:
    json.dump(data, f, indent=2)

# Load
with open("ada.json") as f:
    clone = json.load(f)
print(clone == data)              # True

--------------------------------------------------------
Slide 28  Mini-Project: Contact Manager
--------------------------------------------------------
"""
contacts.py  – CRUD CLI for JSON file
Commands:  add  list  search  delete
"""
import json, sys, pathlib

FILE = pathlib.Path("contacts.json")

def load():
    return json.loads(FILE.read_text()) if FILE.exists() else {}

def save(data):
    FILE.write_text(json.dumps(data, indent=2))

def add(name, phone):
    book = load()
    book[name] = phone
    save(book)
    print(f"Added {name}")

def list_all():
    for name, phone in load().items():
        print(f"{name:15} {phone}")

if __name__ == "__main__":
    cmd = sys.argv[1] if len(sys.argv) > 1 else ""
    match cmd:
        case "add":
            add(sys.argv[2], sys.argv[3])
        case "list":
            list_all()
        case _:
            print("Usage: python contacts.py add|list …")

========================================================
Module 3  ADVANCED
========================================================
Slide 29  Decorators – Function Wrappers
--------------------------------------------------------
def debug(func):
    """Print call signature and return value."""
    import functools
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        args_repr = [repr(a) for a in args]
        kwargs_repr = [f"{k}={v!r}" for k, v in kwargs.items()]
        signature = ", ".join(args_repr + kwargs_repr)
        print(f"Calling {func.__name__}({signature})")
        value = func(*args, **kwargs)
        print(f"{func.__name__} returned {value!r}")
        return value
    return wrapper

@debug
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

gcd(42, 56)

--------------------------------------------------------
Slide 30  Decorators with Arguments
--------------------------------------------------------
def repeat(times: int):
    def decorator(func):
        import functools
        @functools.wraps(func)
        def wrapper(*args, **kwargs):
            for _ in range(times):
                value = func(*args, **kwargs)
            return value
        return wrapper
    return decorator

@repeat(3)
def greet():
    print("Hi!")

greet()

--------------------------------------------------------
Slide 31  Timing & Caching Decorators
--------------------------------------------------------
import time, functools

def timed(func):
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        t0 = time.perf_counter()
        value = func(*args, **kwargs)
        elapsed = time.perf_counter() - t0
        print(f"{func.__name__} took {elapsed*1000:.2f} ms")
        return value
    return wrapper

@functools.lru_cache(maxsize=None)
def fib(n):
    return n if n < 2 else fib(n-1) + fib(n-2)

timed(fib)(35))   # ~0.04 ms after cache warm

--------------------------------------------------------
Slide 32  Generators – Lazy Iteration
--------------------------------------------------------
def evens(limit):
    """Yield even numbers up to limit."""
    value = 0
    while value <= limit:
        yield value
        value += 2

for n in evens(10):
    print(n, end=" ")        # 0 2 4 6 8 10

# Generator expression
squares = (x*x for x in range(10**6))   # no memory blast
import sys
print(sys.getsizeof(squares), "bytes")  # ~200 B

--------------------------------------------------------
Slide 33  Reading Giant Files
--------------------------------------------------------
def parse_access_log(path):
    """Yield dict per line."""
    with open(path) as f:
        for line in f:
            ip, _, _, datetime, method, url, status, size = line.split()[:8]
            yield {
                "ip": ip,
                "datetime": datetime[1:],   # remove [
                "method": method[1:-1],     # remove quotes
                "url": url,
                "status": int(status),
                "size": int(size),
            }

# Process millions of lines
for entry in parse_access_log("access.log"):
    if entry["status"] == 404:
        print(entry["url"])

--------------------------------------------------------
Slide 34  Concurrency Landscape
--------------------------------------------------------
• threading        – concurrent, shared memory, I/O bound  
• multiprocessing – parallel, separate memory, CPU bound  
• asyncio         – single-threaded cooperative, I/O bound, no GIL issues  

--------------------------------------------------------
Slide 35  threading – Download Many Images
--------------------------------------------------------
import threading, requests, time

urls = [f"https://picsum.photos/400/300?random={i}" for i in range(20)]

def download(url):
    resp = requests.get(url, timeout=10)
    filename = url.split("?")[-1] + ".jpg"
    with open(filename, "wb") as f:
        f.write(resp.content)
    print("done", filename)

t0 = time.time()
threads = [threading.Thread(target=download, args=(u,)) for u in urls]
for t in threads: t.start()
for t in threads: t.join()
print("Total:", time.time() - t0, "s")   # ~3 s instead of 30 s

--------------------------------------------------------
Slide 36  multiprocessing – CPU-bound Pi Monte-Carlo
--------------------------------------------------------
import multiprocessing as mp, random

def sample_pi(n):
    """Return hits inside quarter-circle."""
    inside = 0
    for _ in range(n):
        x, y = random.random(), random.random()
        if x*x + y*y <= 1:
            inside += 1
    return inside

def main():
    cores = mp.cpu_count()
    total_samples = 1_000_000
    pool = mp.Pool(cores)
    chunk = total_samples // cores
    counts = pool.map(sample_pi, [chunk]*cores)
    pi_est = 4 * sum(counts) / total_samples
    print("π ≈", pi_est)

if __name__ == "__main__":
    main()

--------------------------------------------------------
Slide 37  asyncio – Concurrent HTTP with aiohttp
--------------------------------------------------------
import aiohttp, asyncio, time

async def fetch(session, url):
    async with session.get(url) as resp:
        return await resp.text()

async def fetch_all(urls):
    async with aiohttp.ClientSession() as session:
        tasks = [asyncio.create_task(fetch(session, u)) for u in urls]
        return await asyncio.gather(*tasks)

if __name__ == "__main__":
    urls = ["https://httpbin.org/delay/1"] * 50
    t0 = time.time()
    pages = asyncio.run(fetch_all(urls))
    print("Fetched", len(pages), "pages in", time.time()-t0, "s")

--------------------------------------------------------
Slide 38  Mixing sync ↔ async
--------------------------------------------------------
def blocking_func():
    time.sleep(1)
    return 42

async def main():
    loop = asyncio.get_running_loop()
    # Run in thread pool so event loop keeps spinning
    result = await loop.run_in_executor(None, blocking_func)
    print(result)

asyncio.run(main())

--------------------------------------------------------
Slide 39  Virtual Environments & Packaging
--------------------------------------------------------
# Create
python -m venv .venv
source .venv/bin/activate        # Windows:  .venv\Scripts\activate

# Upgrade tools
python -m pip install -U pip setuptools wheel

# Install local package
pip install -e .                 # looks for pyproject.toml

--------------------------------------------------------
Slide 40  pyproject.toml (modern replacement for setup.py)
--------------------------------------------------------
[build-system]
requires = ["setuptools>=64", "wheel"]
build-backend = "setuptools.build_meta"

[project]
name = "myutils"
version = "0.1.0"
dependencies = ["requests>=2.28"]

[project.optional-dependencies]
dev = ["pytest", "black", "mypy"]

--------------------------------------------------------
Slide 41  Linting & Formatting
--------------------------------------------------------
pip install black flake8 mypy
black src/ tests/                 # opinionated formatter
flake8 src/                       # style & error checker
mypy src/                         # static type checker

--------------------------------------------------------
Slide 42  Testing with pytest
--------------------------------------------------------
# test_math_utils.py
import pytest
from myutils.math import clamp

@pytest.mark.parametrize("x,lo,hi,expected", [
    (5, 0, 10, 5),
    (-5, 0, 10, 0),
    (15, 0, 10, 10),
])
def test_clamp(x, lo, hi, expected):
    assert clamp(x, lo, hi) == expected

# Run
pytest -q                         # quiet, colored output

--------------------------------------------------------
Slide 43  Type Hints – Gradual Typing
--------------------------------------------------------
from typing import List, Dict, Optional

def freq(words: List[str]) -> Dict[str, int]:
    counts: Dict[str, int] = {}
    for w in words:
        counts[w] = counts.get(w, 0) + 1
    return counts

def find(user_id: int) -> Optional[str]:
    ...

--------------------------------------------------------
Slide 44  Rich REPL with ipython + jupyter
--------------------------------------------------------
pip install ipython
ipython                           # tab-completion, ? help, %magic

jupyter lab                       # browser notebooks
# Inside notebook
%matplotlib inline
import matplotlib.pyplot as plt
plt.plot([1,2,3], [4,5,6])

--------------------------------------------------------
Slide 45  Final Capstone Ideas
--------------------------------------------------------
• Build a REST micro-service with FastAPI  
• Scrape + analyze live data with asyncio & pandas  
• Automate your own boring tasks (rename photos, merge Excel)  
• Deploy a serverless function on AWS Lambda  
• Create a GUI desktop app with textual or PySide6  

--------------------------------------------------------
Slide 46  Keep Climbing
--------------------------------------------------------
Resources
• docs.python.org/3/tutorial/  
• realpython.com  
•pypi.org – 450 k+ packages  
• github.com/python/cpython – read the source!  
• mastodon, /r/python, discord.gg/python  

Remember:  
Read code → Run code → Break code → Fix code → Repeat.  
Happy Pythoning! 🐍