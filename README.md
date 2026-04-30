# John's Math Notes

Searchable study notes for John's IGCSE Edexcel Mathematics tutoring.

## Folder structure
```
john-math-notes/
├── index.html          ← homepage with search
├── notes-index.json    ← list of all notes (you update this)
├── notes/              ← put HTML notes here
│   └── 2026-04-30_quadratics_factoring.html
└── README.md
```

## Adding a new note (workflow per session)

1. Tell Claude (in the project) what topic you taught and the method
2. Claude gives you:
   - An HTML file → save it in `notes/`
   - A JSON line → paste it into `notes-index.json`
3. Open GitHub Desktop, write a commit message like "add quadratics note", click Commit, click Push
4. Wait ~30 seconds, refresh the site — new note appears

## notes-index.json format

Each note is one object in the array. Example:
```json
[
  {
    "file": "2026-04-30_quadratics_factoring.html",
    "title": "Solving Quadratics by Factoring",
    "date": "2026-04-30",
    "tags": ["quadratics", "factoring", "algebra"],
    "summary": "Find roots of x² + bx + c = 0 by splitting into two brackets"
  }
]
```

## Search works across:
- Title (highest weight)
- Tags
- Summary
- Filename
