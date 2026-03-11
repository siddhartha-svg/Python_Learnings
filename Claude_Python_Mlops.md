 # Python — Complete End-to-End Concepts Guide

---

## 🗺️ Python Learning Map Overview

```
Level 1 → Python Basics (Weeks 1-2)
Level 2 → Intermediate Python (Weeks 3-4)
Level 3 → Advanced Python (Weeks 5-6)
Level 4 → Python for Data/ML (Weeks 7-8)
Level 5 → Python for MLOps/Production (Weeks 9-10)
```

---

## 🟢 LEVEL 1: Python Basics
### ⏱️ Time: 2 Weeks

---

### 1️⃣ Setup & Environment
```python
# Tools to install
Python 3.11+
VS Code or PyCharm
Jupyter Notebook / JupyterLab
pip (package manager)
virtualenv / conda (environment manager)

# Create virtual environment
python -m venv myenv
source myenv/bin/activate        # Linux/Mac
myenv\Scripts\activate           # Windows

# Install packages
pip install numpy pandas scikit-learn
pip freeze > requirements.txt    # Save dependencies
```

---

### 2️⃣ Variables & Data Types
```python
# Basic types
name = "Ravi"              # String (str)
age = 25                   # Integer (int)
height = 5.11              # Float (float)
is_employed = True         # Boolean (bool)
nothing = None             # NoneType

# Check type
print(type(name))          # <class 'str'>
print(type(age))           # <class 'int'>

# Type conversion
age_str = str(age)         # int → str
age_float = float(age)     # int → float
num = int("42")            # str → int
```

---

### 3️⃣ Strings — Very Important
```python
name = "Healthcare AI"

# Basic operations
print(len(name))           # Length: 13
print(name.upper())        # HEALTHCARE AI
print(name.lower())        # healthcare ai
print(name.replace("AI", "ML"))  # Healthcare ML
print(name.split(" "))     # ['Healthcare', 'AI']
print(name.strip())        # Remove whitespace

# String formatting (f-strings — most used in ML)
model = "ResNet"
accuracy = 0.956
print(f"Model: {model}, Accuracy: {accuracy:.2f}")
# Output: Model: ResNet, Accuracy: 0.96

# String slicing
text = "Python"
print(text[0])             # P (first char)
print(text[-1])            # n (last char)
print(text[0:3])           # Pyt (slice)
print(text[::-1])          # nohtyP (reverse)

# Check content
print("AI" in name)        # True
print(name.startswith("Health"))  # True
print(name.endswith("AI"))        # True
```

---

### 4️⃣ Numbers & Math
```python
# Arithmetic
print(10 + 3)    # 13 addition
print(10 - 3)    # 7  subtraction
print(10 * 3)    # 30 multiplication
print(10 / 3)    # 3.33 division
print(10 // 3)   # 3  floor division
print(10 % 3)    # 1  modulus (remainder)
print(10 ** 3)   # 1000 power

# Math module
import math
print(math.sqrt(16))       # 4.0
print(math.ceil(4.2))      # 5
print(math.floor(4.8))     # 4
print(math.pi)             # 3.14159...
print(math.log(100, 10))   # 2.0

# Round
print(round(3.14159, 2))   # 3.14
```

---

### 5️⃣ Lists — Most Used in ML
```python
# Create
fruits = ["apple", "banana", "cherry"]
numbers = [1, 2, 3, 4, 5]
mixed = [1, "hello", True, 3.14]
empty = []

# Access
print(fruits[0])           # apple (first)
print(fruits[-1])          # cherry (last)
print(fruits[1:3])         # ['banana', 'cherry']

# Modify
fruits.append("mango")     # Add to end
fruits.insert(1, "grape")  # Add at position
fruits.remove("banana")    # Remove by value
fruits.pop()               # Remove last
fruits.pop(0)              # Remove by index

# Useful operations
print(len(fruits))         # Length
print(sorted(numbers))     # Sort
print(numbers.count(2))    # Count occurrences
print(sum(numbers))        # Sum
print(min(numbers))        # Minimum
print(max(numbers))        # Maximum

# List comprehension (VERY important in ML!)
squares = [x**2 for x in range(10)]
# [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

evens = [x for x in range(20) if x % 2 == 0]
# [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]

# Nested list (like a matrix in ML)
matrix = [[1,2,3], [4,5,6], [7,8,9]]
print(matrix[1][2])        # 6
```

---

### 6️⃣ Tuples
```python
# Immutable list (cannot change after creation)
point = (10, 20)
rgb = (255, 128, 0)

# Access same as list
print(point[0])            # 10

# Unpack
x, y = point
print(x, y)                # 10 20

# Use case in ML: returning multiple values
def get_stats(data):
    return min(data), max(data), sum(data)/len(data)

low, high, avg = get_stats([1,2,3,4,5])
```

---

### 7️⃣ Dictionaries — Critical for ML Config
```python
# Create
model_config = {
    "name": "ResNet50",
    "learning_rate": 0.001,
    "epochs": 100,
    "batch_size": 32
}

# Access
print(model_config["name"])              # ResNet50
print(model_config.get("epochs", 50))   # 100 (with default)

# Modify
model_config["epochs"] = 200           # Update
model_config["optimizer"] = "Adam"     # Add new
del model_config["batch_size"]         # Delete

# Loop
for key, value in model_config.items():
    print(f"{key}: {value}")

# Check key exists
if "learning_rate" in model_config:
    print("LR found!")

# Dict comprehension
squared = {x: x**2 for x in range(5)}
# {0:0, 1:1, 2:4, 3:9, 4:16}

# Nested dict (common in ML configs)
config = {
    "model": {"name": "BERT", "layers": 12},
    "training": {"lr": 0.001, "epochs": 10}
}
print(config["model"]["name"])          # BERT
```

---

### 8️⃣ Sets
```python
# Unique values only
diseases = {"diabetes", "cancer", "diabetes", "fever"}
print(diseases)     # {'diabetes', 'cancer', 'fever'}

# Set operations (useful in data cleaning)
set_a = {1, 2, 3, 4}
set_b = {3, 4, 5, 6}

print(set_a | set_b)   # Union:        {1,2,3,4,5,6}
print(set_a & set_b)   # Intersection: {3,4}
print(set_a - set_b)   # Difference:   {1,2}
```

---

### 9️⃣ Conditionals
```python
# Basic if-else
score = 85

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
else:
    grade = "F"

# One-liner (ternary)
status = "Pass" if score >= 50 else "Fail"

# Logical operators
age = 25
if age >= 18 and age <= 60:
    print("Working age")

if score < 50 or score > 95:
    print("Unusual score")

if not is_employed:
    print("Unemployed")
```

---

### 🔟 Loops
```python
# For loop
for i in range(5):
    print(i)               # 0,1,2,3,4

for i in range(2, 10, 2):
    print(i)               # 2,4,6,8

# Loop over list
models = ["ResNet", "VGG", "BERT"]
for model in models:
    print(model)

# Enumerate (index + value)
for idx, model in enumerate(models):
    print(f"{idx}: {model}")

# While loop
epoch = 0
while epoch < 10:
    print(f"Training epoch {epoch}")
    epoch += 1

# Loop controls
for i in range(10):
    if i == 3:
        continue           # Skip 3
    if i == 7:
        break              # Stop at 7
    print(i)

# Zip (combine two lists)
names = ["Alice", "Bob", "Charlie"]
scores = [90, 85, 92]
for name, score in zip(names, scores):
    print(f"{name}: {score}")
```

---

## 🟡 LEVEL 2: Intermediate Python
### ⏱️ Time: 2 Weeks

---

### 1️⃣ Functions — Core Building Block
```python
# Basic function
def train_model(data, epochs=10, lr=0.001):
    print(f"Training for {epochs} epochs")
    return "model_trained"

# Call function
result = train_model(data, epochs=20)

# *args (variable positional arguments)
def sum_all(*numbers):
    return sum(numbers)

print(sum_all(1, 2, 3, 4, 5))     # 15

# **kwargs (variable keyword arguments)
def create_config(**settings):
    return settings

config = create_config(lr=0.001, epochs=100, model="BERT")
# {'lr': 0.001, 'epochs': 100, 'model': 'BERT'}

# Lambda (one-line function — used a lot in ML)
square = lambda x: x ** 2
print(square(5))               # 25

# Map, Filter, Reduce
numbers = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, numbers))
evens = list(filter(lambda x: x%2==0, numbers))

# Return multiple values
def get_model_stats(predictions, labels):
    accuracy = sum(p==l for p,l in zip(predictions,labels)) / len(labels)
    errors = [i for i,(p,l) in enumerate(zip(predictions,labels)) if p!=l]
    return accuracy, errors

acc, err = get_model_stats([1,0,1,1], [1,0,0,1])
```

---

### 2️⃣ Classes & OOP — Critical for ML Frameworks
```python
# Basic class
class MLModel:
    # Class variable
    framework = "PyTorch"

    # Constructor
    def __init__(self, name, layers, lr=0.001):
        self.name = name          # Instance variable
        self.layers = layers
        self.lr = lr
        self.is_trained = False

    # Method
    def train(self, epochs):
        print(f"Training {self.name} for {epochs} epochs")
        self.is_trained = True
        return self

    def predict(self, data):
        if not self.is_trained:
            raise Exception("Model not trained yet!")
        return f"Prediction from {self.name}"

    # String representation
    def __str__(self):
        return f"MLModel({self.name}, layers={self.layers})"

    def __repr__(self):
        return self.__str__()

# Create instances
model = MLModel("ResNet50", layers=50, lr=0.0001)
model.train(epochs=100)
print(model)               # MLModel(ResNet50, layers=50)

# Inheritance (very common in PyTorch/TensorFlow)
class DeepLearningModel(MLModel):
    def __init__(self, name, layers, lr, gpu=True):
        super().__init__(name, layers, lr)  # Call parent
        self.gpu = gpu

    def train(self, epochs):                # Override method
        device = "GPU" if self.gpu else "CPU"
        print(f"Training on {device}")
        super().train(epochs)              # Call parent method

dl_model = DeepLearningModel("BERT", 12, 0.0001, gpu=True)
dl_model.train(10)
```

---

### 3️⃣ Error Handling — Critical in Production
```python
# Try-Except
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print(f"Math error: {e}")
except Exception as e:
    print(f"Unknown error: {e}")
finally:
    print("Always runs — cleanup here")

# Multiple exceptions
try:
    data = load_medical_data("patient.csv")
    model = load_model("weights.pt")
    predictions = model.predict(data)
except FileNotFoundError as e:
    print(f"File missing: {e}")
except MemoryError:
    print("Not enough RAM for this model")
except Exception as e:
    print(f"Unexpected error: {e}")
    raise                          # Re-raise exception

# Custom exceptions (important in ML pipelines)
class ModelNotTrainedError(Exception):
    pass

class DataValidationError(Exception):
    def __init__(self, message, column):
        super().__init__(message)
        self.column = column

# Raise custom exception
def validate_data(df):
    if df.isnull().any().any():
        raise DataValidationError("Null values found", "age")
```

---

### 4️⃣ File Handling — Essential for ML
```python
# Read text file
with open("data.txt", "r") as f:
    content = f.read()           # Entire file
    lines = f.readlines()        # List of lines

# Write file
with open("results.txt", "w") as f:
    f.write("Model accuracy: 0.95\n")

# Append
with open("logs.txt", "a") as f:
    f.write("Epoch 10 complete\n")

# CSV files (very common in ML)
import csv

# Read CSV
with open("patients.csv", "r") as f:
    reader = csv.DictReader(f)
    for row in reader:
        print(row["age"], row["diagnosis"])

# JSON files (configs, model metadata)
import json

# Read JSON
with open("config.json", "r") as f:
    config = json.load(f)

# Write JSON
model_info = {"name": "ResNet", "accuracy": 0.95}
with open("model_info.json", "w") as f:
    json.dump(model_info, f, indent=4)

# OS and Path operations
import os
from pathlib import Path

# Check if file exists
if os.path.exists("model.pt"):
    print("Model found!")

# Create directory
os.makedirs("models/v1", exist_ok=True)

# List files
files = os.listdir("data/")

# Path manipulation (modern way)
path = Path("data") / "processed" / "train.csv"
print(path.suffix)             # .csv
print(path.stem)               # train
print(path.parent)             # data/processed
```

---

### 5️⃣ Modules & Packages
```python
# Import entire module
import numpy as np
import pandas as pd

# Import specific function
from sklearn.model_selection import train_test_split
from pathlib import Path

# Import everything (avoid in production)
from math import *

# Create your own module (myutils.py)
# ---- myutils.py ----
def preprocess(data):
    return data.dropna()

def evaluate(y_true, y_pred):
    return sum(a==b for a,b in zip(y_true,y_pred)) / len(y_true)

# ---- main.py ----
from myutils import preprocess, evaluate

# __init__.py makes a folder a package
# mypackage/
#   __init__.py
#   preprocessing.py
#   evaluation.py

from mypackage.preprocessing import clean_data
```

---

### 6️⃣ Iterators & Generators — Important for Large Data
```python
# Generator function (memory efficient — critical for large medical datasets)
def data_loader(file_path, batch_size=32):
    batch = []
    with open(file_path) as f:
        for line in f:
            batch.append(line)
            if len(batch) == batch_size:
                yield batch         # Yield instead of return
                batch = []
    if batch:
        yield batch                 # Last partial batch

# Use generator
for batch in data_loader("patients.csv", batch_size=32):
    process_batch(batch)
    # Only 32 rows in memory at a time!

# Generator expression
squares = (x**2 for x in range(1000000))  # No memory used yet!
first_ten = [next(squares) for _ in range(10)]
```

---

## 🔵 LEVEL 3: Advanced Python
### ⏱️ Time: 2 Weeks

---

### 1️⃣ Decorators — Used Everywhere in ML Frameworks
```python
# Basic decorator
def timer(func):
    import time
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"{func.__name__} took {end-start:.2f}s")
        return result
    return wrapper

@timer
def train_model(data):
    # Training code here
    pass

# Decorator with arguments
def retry(max_attempts=3):
    def decorator(func):
        def wrapper(*args, **kwargs):
            for attempt in range(max_attempts):
                try:
                    return func(*args, **kwargs)
                except Exception as e:
                    print(f"Attempt {attempt+1} failed: {e}")
            raise Exception("All attempts failed")
        return wrapper
    return decorator

@retry(max_attempts=3)
def load_model_from_s3(path):
    # Might fail due to network
    pass
```

---

### 2️⃣ Context Managers
```python
# Using with statement (you've seen this)
with open("file.txt") as f:
    data = f.read()

# Create custom context manager
from contextlib import contextmanager

@contextmanager
def ml_experiment(name):
    import mlflow
    print(f"Starting experiment: {name}")
    mlflow.start_run(run_name=name)
    try:
        yield                      # Code inside 'with' runs here
    finally:
        mlflow.end_run()
        print(f"Experiment {name} complete")

# Use it
with ml_experiment("ResNet_Training"):
    model.train(data)
    mlflow.log_metric("accuracy", 0.95)
```

---

### 3️⃣ Comprehensions (All Types)
```python
# List comprehension
squares = [x**2 for x in range(10)]

# Dict comprehension
model_scores = {model: evaluate(model) for model in models}

# Set comprehension
unique_labels = {row["diagnosis"] for row in patient_data}

# Nested comprehension (flatten 2D list)
matrix = [[1,2,3],[4,5,6],[7,8,9]]
flat = [num for row in matrix for num in row]
# [1,2,3,4,5,6,7,8,9]

# Conditional comprehension
passed = [score for score in scores if score >= 50]
grades = ["Pass" if s >= 50 else "Fail" for s in scores]
```

---

### 4️⃣ Regular Expressions — Used in Clinical NLP
```python
import re

text = "Patient DOB: 15/03/1985, BP: 120/80, HR: 72bpm"

# Find patterns
dates = re.findall(r'\d{2}/\d{2}/\d{4}', text)
# ['15/03/1985']

numbers = re.findall(r'\d+', text)
# ['15', '03', '1985', '120', '80', '72']

# Replace (de-identification of medical data!)
clean = re.sub(r'\d{2}/\d{2}/\d{4}', '[DATE]', text)
# "Patient DOB: [DATE], BP: 120/80, HR: 72bpm"

# Check if pattern exists
if re.search(r'BP:\s*\d+/\d+', text):
    print("Blood pressure found!")

# Split
parts = re.split(r',\s*', text)
```

---

### 5️⃣ Logging — Critical for Production ML
```python
import logging

# Setup logging
logging.basicConfig(
    level=logging.INFO,
    format='%(asctime)s - %(name)s - %(levelname)s - %(message)s',
    handlers=[
        logging.FileHandler('ml_pipeline.log'),
        logging.StreamHandler()        # Also print to console
    ]
)

logger = logging.getLogger(__name__)

# Use in ML pipeline
def train_model(data, epochs):
    logger.info(f"Starting training with {len(data)} samples")
    for epoch in range(epochs):
        try:
            loss = run_epoch(data)
            logger.info(f"Epoch {epoch}: loss={loss:.4f}")
        except Exception as e:
            logger.error(f"Training failed at epoch {epoch}: {e}")
            raise
    logger.info("Training complete!")
```

---

### 6️⃣ Multiprocessing & Multithreading
```python
# Threading (good for I/O tasks like downloading data)
import threading

def download_data(url, filename):
    # Download code
    pass

threads = []
urls = ["url1", "url2", "url3"]
for i, url in enumerate(urls):
    t = threading.Thread(target=download_data,
                        args=(url, f"data_{i}.csv"))
    threads.append(t)
    t.start()

for t in threads:
    t.join()               # Wait for all to complete

# Multiprocessing (good for CPU tasks like preprocessing)
from multiprocessing import Pool

def preprocess_patient(patient_data):
    # CPU-intensive processing
    return processed_data

with Pool(processes=4) as pool:
    results = pool.map(preprocess_patient, all_patients)

# Concurrent futures (modern, easiest)
from concurrent.futures import ThreadPoolExecutor, ProcessPoolExecutor

with ProcessPoolExecutor(max_workers=4) as executor:
    futures = [executor.submit(preprocess_patient, p)
               for p in all_patients]
    results = [f.result() for f in futures]
```

---

### 7️⃣ Type Hints — Standard in Production Code
```python
# Type hints make code readable and catch bugs early
from typing import List, Dict, Tuple, Optional, Union

def train_model(
    data: List[Dict],
    epochs: int = 10,
    learning_rate: float = 0.001,
    model_name: Optional[str] = None
) -> Dict[str, float]:

    metrics: Dict[str, float] = {}
    metrics["accuracy"] = 0.95
    metrics["loss"] = 0.05
    return metrics

# Dataclasses (clean config management in MLOps)
from dataclasses import dataclass, field

@dataclass
class TrainingConfig:
    model_name: str
    epochs: int = 100
    learning_rate: float = 0.001
    batch_size: int = 32
    tags: List[str] = field(default_factory=list)

config = TrainingConfig(model_name="ResNet50", epochs=50)
print(config.learning_rate)    # 0.001
```

---

## 🟣 LEVEL 4: Python for Data & ML
### ⏱️ Time: 2 Weeks

---

### 1️⃣ NumPy — Foundation of All ML
```python
import numpy as np

# Create arrays
arr = np.array([1, 2, 3, 4, 5])
matrix = np.array([[1,2,3],[4,5,6],[7,8,9]])
zeros = np.zeros((3, 4))
ones = np.ones((2, 3))
random = np.random.rand(3, 3)
range_arr = np.arange(0, 10, 2)   # [0,2,4,6,8]

# Shape operations
print(matrix.shape)        # (3, 3)
print(matrix.ndim)         # 2
print(matrix.dtype)        # int64
reshaped = matrix.reshape(1, 9)

# Math operations (all element-wise)
print(arr * 2)             # [2,4,6,8,10]
print(arr + arr)           # [2,4,6,8,10]
print(np.sqrt(arr))        # Square root
print(np.exp(arr))         # Exponential

# Statistics
print(np.mean(arr))        # 3.0
print(np.std(arr))         # Standard deviation
print(np.min(arr))         # 1
print(np.max(arr))         # 5
print(np.sum(arr))         # 15

# Indexing & slicing
print(matrix[0, :])        # First row
print(matrix[:, 1])        # Second column
print(matrix[0:2, 0:2])    # Sub-matrix

# Boolean indexing (very common in ML)
arr = np.array([1,5,3,8,2,9])
print(arr[arr > 4])        # [5,8,9]
```

---

### 2️⃣ Pandas — Data Manipulation
```python
import pandas as pd

# Create DataFrame
df = pd.DataFrame({
    "patient_id": [1, 2, 3, 4, 5],
    "age": [45, 32, 67, 28, 55],
    "diagnosis": ["diabetes", "healthy", "ca
