# Korean Vocabulary Practice

Open `korean.html` in a browser. On each page load, the app asks you to choose a vocabulary database. Select **Load vocabulary CSV** or use the visible file picker to choose `data_base.csv`, `data_base_new_words.csv`, or another compatible CSV. Practice controls stay disabled until a valid database is loaded; no database loads automatically.

Select **Load vocabulary CSV** at any time to switch databases, including `data_base_new_words.csv`. The selected file's name and word count appear above the card. Loading a valid database refreshes categories and starts a new session with zero scores. Canceling the picker or choosing an invalid file preserves the current practice session.

To serve the page locally instead of opening the HTML file directly, run this command from this folder:

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
