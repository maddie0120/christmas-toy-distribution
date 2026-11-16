# 🎁 christmas-toy-distribution

## 📋 Project Overview

The goal of this project is to maximize the number of children who receive a requested toy from Santa's distribution network, while respecting factory production capacities and international trade restrictions.

The problem is modeled as a **Linear Programming (LP)** optimization problem and solved using Python and the PuLP library.

## 📥 Input Format

The input consists of:

1. Three integers `n`, `m`, and `t`, representing the number of factories, countries, and children, respectively.
2. `n` lines describing each factory:
   - Factory ID.
   - Country ID where the factory is located.
   - Maximum number of toys it can produce.
3. `m` lines describing each country:
   - Country ID.
   - Maximum number of toys that can be exported.
   - Minimum number of gifts that must be delivered within the country.
4. `t` lines describing each child:
   - Child ID.
   - Country ID where the child lives.
   - IDs of the factories producing toys requested by that child.

## 📤 Output Format

The program outputs a single integer:

- The maximum number of children whose requests can be satisfied while respecting all constraints.
- `-1` if the constraints cannot be satisfied.

## 🎯 Problem Constraints

The distribution plan must satisfy the following conditions:

- Each factory cannot distribute more toys than its maximum production capacity.
- Each child can receive at most one toy, and it must be one of the toys they requested.
- Each country must receive at least its required minimum number of gifts.
- The total number of toys exported from factories in each country cannot exceed that country's export limit.

The objective is to maximize the total number of children who receive a requested toy.

## 📌 Example

**Input:**

```text
3 2 3
1 1 1
2 1 1
3 2 1
1 2 1
2 2 1
1 1 2 3
2 1 2 1
3 2 1
```

**Output:**

```text
3
```

## ⚙️ How to Run

### 🔧 1. Install Requirements

Make sure Python 3 and `pip` are installed.

Install the PuLP library:

```bash
python3 -m pip install pulp
```

A compatible LP solver is also required. For example, on Ubuntu, install GLPK:

```bash
sudo apt-get install glpk-utils
```

### ▶️ 2. Run the Program

Execute the program using an input file:

```bash
python3 projeto.py < input.txt
```

Replace `input.txt` with the path to the desired input file.

## 👥 Authors

<p align="center">
  <a href="https://github.com/maddie0120">
    <img src="https://img.shields.io/badge/Madalena%20Yang-@maddie0120-blue?style=for-the-badge&logo=github" alt="Madalena Yang GitHub"/>
  </a>
  &nbsp;&nbsp;&nbsp;
  <a href="https://github.com/xan-verse">
    <img src="https://img.shields.io/badge/Alexandre%20Delgado-@xan--verse-blue?style=for-the-badge&logo=github" alt="Alexandre Delgado GitHub"/>
  </a>
</p>

## 📚 Project Description

The original project statement is available [here](p3.pdf).
