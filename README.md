## 🔧 Regex Engine from Scratch in Python

**Regex Compiler | Thompson’s NFA | DFA Optimization | CS Fundamentals**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1L0dXvuL42HrzCOjJXOAAsxDk6XG5HE7e?usp=sharing)

> 🔗 Click the badge above to run the complete Regex Engine notebook with NFA/DFA visualization and benchmarks on Google Colab.

---

## 🚀 Overview

This project implements a **regex engine** from scratch — mimicking how languages like Python, JavaScript, and C internally parse and match regex expressions.

It supports:
- ✅ Concatenation (`ab`)
- ✅ Alternation (`a|b`)
- ✅ Kleene star & plus (`a*`, `a+`)
- ✅ Grouping (`(ab)*`)
- ✅ Wildcard (`.`)
- ✅ Basic repetition (`a{n}`, `a{x,y}` coming soon)

The engine is built in pure Python and does **infix → postfix conversion**, constructs an **NFA using Thompson’s algorithm**, optionally converts it to a **DFA**, and runs full pattern matching on input strings.

---

## 🧠 Key Features

- 🔄 Converts infix regex to postfix using **Shunting Yard algorithm**
- ⚙️ Constructs an **NFA from postfix regex** using Thompson’s Construction
- 🧠 Supports **ε-transitions**, **nested grouping**, and **greedy repetition**
- ⚡ Includes **NFA → DFA optimization** using subset construction
- 🎨 Visualizes both **NFA and DFA** using Graphviz
- 🧪 Provides a **unified test harness and performance benchmark**

---

## 🎯 Sample Regex Patterns

| Regex         | Input       | Expected | Match Engine |
|---------------|-------------|----------|--------------|
| `a(b|c)*d`    | `abbd`      | ✅ True  | NFA + DFA    |
| `ab*`         | `abbb`      | ✅ True  | NFA + DFA    |
| `(a|b)*c`     | `aabbc`     | ✅ True  | NFA + DFA    |
| `a+`          | `aaa`       | ✅ True  | NFA + DFA    |
| `a+`          | `""`        | ❌ False | NFA + DFA    |

---


> DFA is 6–10x faster on average for repeated match operations.

---

## 🎨 Visualizations

### 🧠 NFA Graph

*Rendered directly in Colab using Graphviz*

### ⚙️ DFA Graph

*Each node shows a set of NFA states. Accept states are green and double-circled.*

---

## 🧰 Tech Stack

| Tool         | Role                           |
|--------------|--------------------------------|
| Python 3.10+ | Core language                  |
| Graphviz     | Automata visualization         |
| Google Colab | Interactive development        |
| `time`       | Performance benchmarking       |

---

## 🧪 Internal Structure

1. `regex_parser.py` – Converts infix regex to postfix  
2. `nfa.py` – Thompson NFA builder  
3. `matcher.py` – NFA simulation  
4. `dfa.py` – Subset construction for DFA  
5. `visualizer.py` – Graphviz for NFA/DFA  
6. `tests.py` – Unified harness and benchmark runner  

---

## 🚀 How to Run

1. Open in Google Colab using the badge above  
2. Run top-down: parser → NFA → DFA → tests → benchmark  
3. Modify patterns or input to test your own cases  
4. Export graphs via `.render()` if needed

---

## 🌱 Future Scope

- Add full `{n}` and `{x,y}` repetition support  
- Add backtracking visualizer  
- Package as a pip installable CLI tool  
- Compile to bytecode or integrate with tokenizer/lexer  
- Deploy with Gradio or Flask API  

---

## 📄 License

MIT License  
Feel free to use, fork, or contribute.
""" 

## 👩‍💻 Author

**Sanskriti Kumari**  
Mentor & Head of Ops @ Naariverse  
🔗 [LinkedIn](https://www.linkedin.com/in/sanskriti-kumari/)  

---
