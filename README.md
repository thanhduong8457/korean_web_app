# Chinese Vocabulary Practice

Run the app from this folder with a local HTTP server:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000/chinese.html. If you open `chinese.html` directly and your browser blocks loading local files, choose the adjacent `new_word.md` with the file picker shown on the page.

The app reads vocabulary from `new_word.md` automatically. Each nonblank line uses `Simplified【Traditional】[Pinyin] Vietnamese meaning`. The Traditional form and Pinyin are optional. Invalid and duplicate lines are skipped, with line numbers shown in the loading status. The original Markdown and CSV files are never changed; `data_base.csv` is not loaded.

- Choose Chinese → Vietnamese or Vietnamese → Chinese and type an answer. Enter checks it, then Enter advances to the next question.
- Vietnamese answers ignore case and normalize Unicode while preserving accents. Commas, semicolons, and spaced slashes in a source meaning explicitly list accepted alternatives.
- Chinese answers accept the Simplified form and the Traditional form when one is listed. Pinyin is shown after answering but is not accepted as a Chinese answer.
- Review flashcards keeps card flipping, pronunciation, and remembered/practice-again ratings. Pronunciation depends on browser speech support and available Chinese voices.
- Session progress counts typed answers across both practice modes. Restart session or reload the page to clear it.
