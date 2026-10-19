# Language Vocabulary Practice

Open `language_practice.html` in a browser. Choose **Load vocabulary CSV** or use the file picker to select a Korean or Chinese CSV. No vocabulary loads automatically, and an invalid file leaves the current session in place. Loading a valid file starts a new session and sets the practice modes for that language.

Included files:

- `data_base.csv`, `lesson_06_vocabulary.csv`, `lesson_07_vocabulary.csv`, and `unit7_appoitment.csv` contain Korean vocabulary.
- `chinese_vocabulary.csv` contains the 20 Chinese entries from `chinese_branch/new_word.md`. The original `new_word.md` is retained as source material.

CSV headers determine the language:

- Korean: required `Korean` and `English`; optional `Category`.
- Chinese: required `Simplified` (or `Chinese`) and `Vietnamese`; optional `Traditional`, `Pinyin`, `Category`, and `Example`.

Other columns are ignored. Blank, malformed, incomplete, and duplicate rows are skipped. A file must contain at least one usable entry. The app does not change source files.

Choose a direction and optionally filter by category. Press Enter to check an answer, then Enter again to advance. An empty answer reveals the solution and counts as incorrect. Switching modes preserves session scores; loading another CSV or selecting **Restart session** clears them. Flashcard review, pronunciation, and remembered/practice-again ratings remain available.

For Korean, English answers ignore case, extra whitespace, and final punctuation; spaced slash alternatives and optional parenthetical explanations work as before. For Chinese, Vietnamese answers ignore case and normalize Unicode while keeping accents. Commas, semicolons, and spaced slashes explicitly list Vietnamese alternatives. Chinese answers accept the listed Simplified or Traditional form, but not Pinyin.

The page can be opened directly because it uses a file picker. To serve it locally, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Then open http://127.0.0.1:8000/language_practice.html. Pronunciation requires browser speech support and a suitable Korean or Chinese voice.
