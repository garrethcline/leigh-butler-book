# The Leigh Household Butler Book

My capstone project at The International Butler Academy (February to April 2026): an operations manual for a fictional family with three homes in New York and Toronto. It has step-by-step standard operating procedures for each home, cleaning standards, scoring guides for staff and vendors, and the daily working documents a butler would use. It received the highest capstone grade in my cohort.

Read it online: https://garrethcline.github.io/leigh-butler-book/

## How it was written

I wrote the book with AI tools, and the book says so in its front matter. I set the household, the structure and the standards, and gave the AI my course notes and research. The AI drafted, formatted and illustrated sections, and I checked and edited them. The web reader in this repository was built the same way.

## Files

- `index.html`: the landing page.
- `reader.html`: the reader. It loads epub.js and JSZip from public CDNs, opens the book in the browser and remembers where you stopped.
- `Leigh_Butler_Book.epub`: the book.

To run it on your own computer, serve the folder with any static web server (for example `python -m http.server`) and open `index.html`. Opening the file directly may not work, because the reader fetches the EPUB over HTTP.

The Leigh family, their staff and their homes are invented. Some brands and service providers named in the book are real.

Garreth Cline, 2026
