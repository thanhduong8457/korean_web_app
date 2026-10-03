# Korean Vocabulary Practice

Open `korean.html` in a browser. If automatic loading is blocked, choose the adjacent `data_base.csv` using the file picker shown on the page.

For automatic loading, run this command from this folder:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Then visit http://127.0.0.1:8000/korean.html.

- Choose Korean → English or English → Korean, optionally filter by category, and type an answer.
- Press Enter to check; press Enter again or select Next word to continue.
- Spaced slash alternatives are accepted individually. English matching ignores case and optional parenthetical explanations. Both directions ignore extra whitespace and final sentence punctuation, and normalize Unicode.
- Category labels distinguish native and Sino-Korean numbers with the same English meaning.
- Review flashcards retains pronunciation, card flipping, and remembered/practice-again ratings. Pronunciation depends on browser speech support and installed Korean voices.
- Scores cover typed answers in both modes for the current page session. Switching modes or categories preserves scores; Restart session or reloading the page clears them. Existing CSV history is not changed or included in session totals.

The app uses the CSV's `Korean`, `English`, and optional `Category` columns. Blank, incomplete, malformed, and duplicate records are handled without hard-coded vocabulary. There are no external dependencies.
