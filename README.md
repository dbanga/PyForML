# Python Refresher Lab — FAANG-Level Hands-On

**Goal:** Refresh Python fundamentals + interview patterns the way FAANG expects ML engineers to code.

**Outcome:** Students can write clean, efficient, interview-ready Python and explain tradeoffs (time/space, data structure choice, gotchas).

---

# How to Start

1. **Fork** this repository.  
2. Open `python_refresher_student_lab.ipynb` in **Google Colab**.  
3. Complete all **TODO** sections.  
4. **Restart runtime → Run All** cells.  
5. Push changes and submit a **Pull Request**.  

⚠️ **Do NOT edit notebooks directly on GitHub.**

---

## Lab Rules (FAANG Style)

- ❌ No “works on my machine” code (write deterministic tests)
- ✅ Always analyze time & space complexity
- ✅ Prefer a clean baseline first, then optimize
- ✅ Handle edge cases explicitly
- ✅ Use the right data structure (dict/set/heap/deque)

---

# Out of Scope

- External libraries (unless explicitly imported)
- ML model training

---

# Notebook Rules

- Do **NOT** rename the notebook  
- Do **NOT** delete TODOs  
- Do **NOT** hardcode outputs  
- Notebook must run **top-to-bottom**  

---

# Dataset

- Synthetic Python inputs only

## Why?

- Mirrors FAANG interview settings
- Forces focus on algorithm + complexity

---

## Section 1 — Python Idioms & Data Structures

### Task 1.1: Comprehensions

Create (without unnecessary loops):

- Squares of even numbers from 1..20
- List of (x, x²) for x=1..10
- Flatten a nested list

**Checkpoint Questions:**

- When do generator expressions beat list comprehensions?
- Why can Python-level loops be slower?

---

### Task 1.2: `Counter` and frequency counting

- Count characters in a string
- Extract top-k most common

**Interview Angle:**

- `Counter` vs sorting (time complexity)
- When is hashing a bottleneck?

---

### Task 1.3: `defaultdict` grouping

- Group words by first letter
- Build nested groupings

**FAANG Gotcha:**

- Difference between basic slicing vs “missing key” errors in dict

---

## Section 2 — FAANG Core Patterns

### Task 2.1: Two Sum (Hash Map)

- O(n) one-pass hash map

**Checkpoint Questions:**

- Why does the order “check complement then insert” matter?
- What breaks if duplicates exist?

---

### Task 2.2: Longest Substring Without Repeating Characters (Sliding Window)

- Maintain a moving window with an invariant

**Checkpoint Questions:**

- What is the window invariant?
- Why is the algorithm O(n) and not O(n²)?

---

### Task 2.3: Product of Array Except Self (Prefix/Suffix)

- No division
- O(n)

**Interview Angle:**

- Why does it handle zeros naturally?

---

## Section 3 — FAANG Hard (Optional)

### Task 3.1: Sliding Window Maximum (Deque)

**FAANG Gotcha:**

- Explain why deque ops are amortized O(n)

---

### Task 3.2: LRU Cache (Hash Map + Doubly Linked List)

**FAANG Gotcha:**

- O(1) `get`/`put` requires both structures

---

## Submission Expectations

Students must submit:

- Clean notebook (runs top-to-bottom)
- Short answers for each **Checkpoint/Explain** block
- Complexity notes for each core problem

---

## FAANG Interview Evaluation Rubric

| Skill                         | Evaluated |
|------------------------------|-----------|
| Data structure choice         | ✅        |
| Complexity reasoning          | ✅        |
| Edge-case coverage            | ✅        |
| Correctness & invariants      | ✅        |
| Code clarity                  | ✅        |
| Communication (explanations)  | ✅        |

---

## Stretch Problems (Optional)

- Merge K Sorted Lists (heap)
- Validate Parentheses (stack)
- Implement `topKFrequent` with heap vs bucket sort
