# King James Version (1769) — JSON Dataset

A public domain, machine readable dataset of the **1769 King James Version (KJV) Bible**, containing the 66 books of the Old and New Testaments.

The text is organized by book, chapter, and verse in JSON format. It is provided by **Saorsa Industries** for anyone to use, adapt, analyze, or incorporate into their own projects, for any purpose.

## Contents

The repository includes **66 book files**, **1,189 chapters**, and **31,102 verse records**.

```text
├── books/
│   ├── Genesis.json
│   ├── Exodus.json
│   ├── ...
│   └── Revelation.json
├── books.json
└── books_chapter_count.json
```

- **`books/`** — One JSON file per book, containing its chapters and verses.
- **`books.json`** — Ordered list of book names.
- **`books_chapter_count.json`** — Book names and their chapter counts.

## JSON Format

Each book file follows this structure (example abridged):

```json
{
  "book": "Genesis",
  "chapters": [
    {
      "chapter": 1,
      "verses": [
        {
          "verse": 1,
          "text": "In the beginning God created the heaven and the earth."
        }
      ]
    }
  ],
  "chapter-count": "50"
}
```

The `chapter-count` field is a string; chapter and verse numbers are integers. The text is presented as contained in this dataset, including its spelling and punctuation.

## Example Usage

Read a book and print its first verse using Python:

```python
import json

with open("books/Genesis.json", encoding="utf-8") as file:
    genesis = json.load(file)

print(genesis["chapters"][0]["verses"][0]["text"])
```

No additional Python packages are required.

## Potential Uses

This dataset may be used for **any purpose**, including Bible applications, reading tools, search engines, concordances, textual comparison, linguistics, natural language processing (NLP), machine learning, semantic search, digital humanities, educational resources, and other research or software projects. These are examples, not restrictions.

## Public Domain and License

The King James Version text is in the public domain in the United States. Saorsa Industries makes its own contributions to this dataset available under the [Creative Commons CC0 1.0 Universal Public Domain Dedication](https://creativecommons.org/publicdomain/zero/1.0/). No permission or attribution from Saorsa Industries is required.

Users outside the United States should verify applicable local rules, including special rights concerning the Authorized Version in the United Kingdom. CC0 does not waive third-party rights.

## Maintainer

**Saorsa Industries**  
https://saorsaindustries.com
