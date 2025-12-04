# Weekend Python Crash Course 🐍  
## Day 3 Trainer Guide – OOP, Libraries & Mini Projects

---

## 🕒 Schedule Overview (Day 3)

| Time | Topic | Format |
|------|-------|--------|
| 9:00 – 9:45 AM | Object-Oriented Programming (OOP) Basics | Presentation + Demo |
| 9:45 – 10:30 AM | OOP Exercises | Lab / Pair Programming |
| 10:30 – 11:00 AM | Break | — |
| 11:00 – 12:00 PM | Python Libraries – Standard & Optional | Demo + Exercises |
| 12:00 – 12:30 PM | Library Exercises | Lab |
| 12:30 – 1:30 PM | Lunch | — |
| 1:30 – 3:00 PM | Mini Projects | Guided Coding + Independent Work |
| 3:00 – 4:15 PM | Mini Project Development | Independent Coding with Instructor Support |
| 4:15 – 4:45 PM | Wrap-Up & Optional Challenges | Discussion / Q&A |
| 4:45 – 5:00 PM | End-of-Day Review | Summary / Tips / Resources |

---

## 📝 Instructor Notes

### **Object-Oriented Programming (OOP)**
- Key concepts: **class**, **object**, **attributes**, **methods**  
- Explain `__init__` for initializing object attributes  
- Demonstrate object creation and method calls  
- Encourage learners to create multiple objects to see differences  

**Tips:**
- Use relatable examples: Person, Car, BankAccount  
- Highlight the difference between functions and methods in classes  

---

### **Python Libraries**
- **random**: random numbers, choices, shuffling  
- **datetime**: current date/time, formatting  
- **math**: sqrt, power, factorial  
- **pandas**: optional, data manipulation with DataFrame  
- **requests**: optional, fetch API data  

**Tips:**
- Demonstrate one library at a time with simple, clear examples  
- Show common mistakes (e.g., forgetting to import modules) and how to fix them  

---

### **Mini Projects**
- Encourage breaking the project into **steps**: functions, then classes, then combining  
- Provide hints rather than full solutions to encourage problem-solving  
- Suggest enhancements for advanced learners:  
  - Score tracking, leaderboard, file storage  
  - Additional features like random events, data visualization  

---

## ✅ Exercise Solutions (Examples)

### OOP Exercises
```python
# Car class
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def display_info(self):
        print(f"{self.year} {self.make} {self.model}")

    def age(self, current_year):
        return current_year - self.year

car1 = Car("Toyota", "Corolla", 2018)
car2 = Car("Honda", "Civic", 2020)
car1.display_info()
car2.display_info()
print("Car1 age:", car1.age(2025))
````

### Python Libraries

```python
# random
import random
dice1 = random.randint(1,6)
dice2 = random.randint(1,6)
print("Dice sum:", dice1 + dice2)

# datetime
from datetime import datetime
now = datetime.now()
print(now.strftime("%Y-%m-%d %H:%M"))

# math
import math
print(math.sqrt(16), math.factorial(5), math.pow(2,3))

# pandas (optional)
import pandas as pd
data = {"Name": ["Alice", "Bob", "Charlie"], "Age": [25,30,22]}
df = pd.DataFrame(data)
print(df)
```

### Mini Projects – Hints

* **Quiz Game**: Use a list of Question objects, loop through, keep score
* **Budget Tracker**: Use a class to manage income/expenses, calculate total balance
* Encourage saving projects in separate folders

---

## 💡 Tips for Trainers

* Keep sessions interactive and hands-on
* Offer real-time debugging assistance
* Encourage learners to explain their code to peers
* Reinforce concepts by asking questions: "What does this method do?"
* Highlight real-world application of OOP and libraries

---

## 📚 Resources

* [Python Official Documentation – Classes](https://docs.python.org/3/tutorial/classes.html)
* [Automate the Boring Stuff with Python – Classes & Modules](https://automatetheboringstuff.com/)
* [Python Standard Library Documentation](https://docs.python.org/3/library/)
* [Pandas Documentation](https://pandas.pydata.org/docs/)

---


