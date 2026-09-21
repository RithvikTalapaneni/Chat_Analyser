# Chat_Analyser
# GroupDNA 🧬

> A WhatsApp Group Analytics tool built with Python fundamentals and
> NumPy --- turning a raw WhatsApp chat export into an activity,
> vocabulary, response-pattern, and personality report.

## 📌 Project Overview

**GroupDNA** analyzes a WhatsApp group chat exported as a `.txt` file
and produces a clean, text-based analytical report.

The project was built as a minor project with a deliberate constraint:
solve a realistic data-analysis problem **without relying on heavy
data-science libraries**.

The supplied `hostel_bois.txt` dataset contains **3,174 real participant
messages from 6 participants over 60 days**. The parser also handles
WhatsApp-specific cases such as system messages, media placeholders, and
deleted-message entries.

## ✨ Features

### 1. Chat Parser

-   Reads the WhatsApp `.txt` export.
-   Extracts timestamp, sender, and message text.
-   Separates participant messages from system messages.
-   Handles media and deleted-message entries according to the project
    rules.

### 2. Group Overview

-   Total messages
-   Date range
-   Number of active participants
-   Per-person message counts
-   Per-person word-count and average-message-length statistics

### 3. Activity Analysis

-   Most active day
-   Most active hour
-   Per-person activity patterns

### 4. NumPy Activity Heatmap

Creates a **6 × 24 NumPy matrix** representing message activity by
participant and hour, then renders it as a terminal-friendly text
heatmap using shading characters.

### 5. Top Words

-   Normalizes words to lowercase.
-   Removes punctuation.
-   Uses a custom stop-word list.
-   Finds the group's top 10 words.
-   Supports per-person vocabulary analysis.
-   Can render word frequencies using text bars.

### 6. Response Speed & Silent Streaks

-   Calculates average response gaps using `datetime`.
-   Identifies the fastest/slowest repliers.
-   Finds each participant's longest consecutive silent streak.

### 7. Personality Archetypes

Each participant receives one highest-scoring archetype based on
quantitative rules:

-   🔥 **THE SPAMMER**
-   ❤️ **THE GROUP MOM**
-   🌙 **THE NIGHT OWL**
-   📖 **THE STORYTELLER**
-   🎭 **THE DRAMA QUEEN**
-   👻 **THE GHOST**
-   😂 **THE COMEDIAN**
-   ❓ **THE QUESTION MASTER**

For the supplied dataset, the intended major classifications are:

  Participant   Archetype
  ------------- -----------------
  Rahul         THE SPAMMER
  Priya         THE GROUP MOM
  Aman          THE NIGHT OWL
  Karan         THE STORYTELLER
  Neha          THE DRAMA QUEEN
  Vikas         THE GHOST

### 8. Final Report

Combines the analysis into a formatted console report designed to be
easy to read and screenshot.

------------------------------------------------------------------------

## 🛠️ Tech Stack

-   Python
-   NumPy
-   `datetime`
-   File I/O
-   Lists, dictionaries, sets, tuples
-   Loops and conditionals
-   String manipulation
-   Functions
-   List/dictionary comprehensions
-   `sorted()`, `lambda`, and f-strings

## 🚫 Deliberate Constraints

This project intentionally does **not** use:

-   ❌ pandas
-   ❌ matplotlib
-   ❌ seaborn
-   ❌ plotly
-   ❌ `collections.Counter`
-   ❌ `collections.defaultdict`
-   ❌ regular expressions (`re`)
-   ❌ NLTK
-   ❌ scikit-learn / ML libraries
-   ❌ pre-built WhatsApp analyzer libraries
-   ❌ external chat datasets

The text heatmap is implemented with NumPy and terminal characters
instead of a plotting library.

## 📂 Repository Structure

``` text
GroupDNA/
│
├── GroupDNA.ipynb
├── hostel_bois.txt
├── README.md
└── output/
    └── screenshot.png
```

> Rename the notebook in the structure above if your actual notebook has
> a different filename.

## ▶️ How to Run

### Option 1 --- Google Colab

1.  Open the notebook in Google Colab.
2.  Upload `hostel_bois.txt` to the Colab file area.
3.  Run the notebook cells from top to bottom.
4.  The final GroupDNA report will be printed in the notebook output.

### Option 2 --- Jupyter Notebook

1.  Clone/download this repository.
2.  Place `hostel_bois.txt` in the expected project directory.
3.  Open the `.ipynb` notebook in Jupyter.
4.  Run all cells.

Make sure Python and NumPy are installed.

## 📊 Dataset

The project uses the supplied `hostel_bois.txt` dataset.

The parser checkpoint is **3,174 participant messages**, with 6
participants across a 60-day chat period.

The dataset is used for the project analysis and is not replaced with an
external dataset.

## 🧠 Why This Project?

GroupDNA started as a simple question:

> **What can we actually learn from the way a friend group chats?**

Instead of treating a WhatsApp export as just text, GroupDNA turns it
into structured data and asks questions about activity, vocabulary,
response behavior, silence, and personality patterns.

The interesting part is not only the final report --- it is building the
parser and analytical logic from fundamentals under strict constraints.

## 📈 Key Learning Outcomes

-   Parsing semi-structured real-world text data
-   Designing reusable analysis functions
-   Building counters with dictionaries
-   Working with timestamps and time differences
-   Using NumPy for matrix-based analysis
-   Designing rule-based classification
-   Handling messy input and edge cases
-   Presenting analytical results clearly



## 📜 Project Requirements

This project follows the GroupDNA Minor Project Brief requirements,
including the eight mandatory features, NumPy heatmap,
restricted-library rules, and README/repository requirements.

------------------------------------------------------------------------

**Built with Python fundamentals + NumPy. No pandas. No matplotlib. No
regex. Just data, logic, and a lot of messages. 🧬**

