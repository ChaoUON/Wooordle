# Wooordle

A lightweight, browser-based vocabulary game inspired by Wordle, designed for practising word meanings using custom word lists.

This project is **purely static** (HTML + TXT) and requires **no backend and no build step**.

---

## 🔗 Live Demo

https://chaouon.github.io/Wooordle/

---

## ✨ Features

- 🎮 **Wordle-style gameplay** — Guess x-letter words based on definitions
- 📚 **Custom dictionaries** — Import your own vocabulary files (`.txt` format)
- 💡 **Hint system** — Get hints for category, definition, or example sentence
- ⏱️ **Optional timer** — Set time limits for added challenge
- 📊 **Session statistics** — Track success rate, attempts, and progress
- 🏷️ **Word categorization** — Organize vocabulary by categories and subcategories
- 🎯 **Session configuration** — Choose number of words per session
- 💾 **Session persistence** — Statistics saved across sessions
- 🌐 **Fully static** — No backend required, works entirely in the browser

---

## 🚀 Getting Started

### Quick start

1. **Open the game** — Visit the [live demo](https://chaouon.github.io/Wooordle/) or open `index.html` locally in your browser
2. **Import a dictionary** — Click the **📖 Settings** button to load a vocabulary file
3. **Configure your session** — Set the number of words (default: 10)
4. **Start playing** — Guess the word based on the definition
5. **Use hints** — Click category, definition, or example hints if needed

### How to play

1. You will see a definition and example sentence for a hidden word
2. Guess the word by typing letters and pressing Enter
3. The game shows you:
   - **🟩 Green** — correct letter in the correct position
   - **🟨 Yellow** — correct letter in wrong position
   - **⬜ Gray** — letter not in the word
4. You have **6 attempts** per word
5. After completing or skipping a word, move to the next one with **Next Word**
6. View your session statistics when complete

### Optional settings

- **⏱️ Timer** — Enable timer and set duration (in seconds) for added challenge
- **💡 Hints** — Enable/disable the hint system
- **Words per session** — Choose between 5 and 50 words

---

## 📁 Project Structure

```
wooor-dle/
  index.html
  atom_300_vocab.txt
  README.md
  LICENSE
```

- `index.html` — main game page  
- `atom_300_vocab.txt` — sample vocabulary list (structured plain text)

---

## 📥 Vocabulary File Format

Vocabulary files are plain text (`.txt`) files in a **structured dictionary format**.

### File structure

The file may optionally start with metadata lines, followed by category headers and vocabulary entries:

```
FORMAT: AtomVocab-1
FIELDS: number | word | part_of_speech | definition | example
HEADERS: [Category] / [Subcategory]
```

---

### Category headers

Categories and subcategories are specified as:

```
[Category] | category name
[Subcategory] | subcategory name
```

Example:
```
[Category] | Characters and their emotions
[Subcategory] | Positive emotions
```

---

### Vocabulary entries

Each vocabulary entry is written on a single line using **pipe (`|`) separators**, with fields in the following order:

```
number | word | part_of_speech | definition | example
```

Example:
```
1 | amused | adjective | Finding something entertaining or funny. | He gave an amused chuckle at his sister’s dramatic storytelling.
2 | empathetic | adjective | Deeply understanding of another person’s feelings. | His empathetic nature made him a great friend.
```

---

### Notes

- Whitespace around `|` is ignored  
- Definitions and examples may contain spaces and punctuation  
- Category and subcategory headers apply to all following entries until changed  
- The exact parsing behaviour depends on the game version

---

## 📚 Sample Vocabulary Source and Attribution

The **300 vocabulary words themselves** originate from the following public educational resource:

- *11+ vocabulary: 300 words your child should know*  
  Atom Learning  
  https://atomlearning.com/blog/11-plus-vocabulary

The file included in this repository, **`atom_300_vocab.txt`**, is a **restructured and reformatted dictionary-style representation** created for use in this game.

This sample vocabulary file is provided **solely for demonstration and educational purposes**.

Users are encouraged to use their own vocabulary lists when using or redistributing this project.

---

## 📜 Licence

This project is licensed under the **Creative Commons Attribution–NonCommercial 4.0 International (CC BY-NC 4.0)** licence.

Commercial use is **not permitted**.

---

## ✨ Credits

Created by C. Chen.  
Inspired by Wordle-style vocabulary learning.
