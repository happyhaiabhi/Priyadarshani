# Priyadarshani BPSC PYQ Quiz 📚

A clean, chapter-wise MCQ quiz website built for BPSC Prelims preparation using the **Priyadarshani Book Series** question bank.

## 🗂 Project Structure

```
quiz-site/
├── index.html          ← Home page (subject + chapter selector)
├── quiz.html           ← Quiz engine
├── css/
│   └── style.css       ← All styling (dark academic theme)
├── js/
│   ├── app.js          ← Home page logic
│   └── quiz.js         ← Quiz engine logic
└── data/
    ├── chapters.json         ← Master index (auto-generated; do not edit manually)
    ├── modern_history.json   ← Modern History MCQs
    ├── ancient_history.json  ← Ancient History MCQs
    ├── polity.json           ← Indian Polity MCQs
    ├── economy.json          ← Indian Economy MCQs
    ├── world_geography.json  ← World Geography MCQs
    ├── bihar_special.json    ← Bihar Special MCQs
    ├── math.json             ← Mathematics MCQs
    ├── physics.json          ← Physics MCQs
    └── biology.json          ← Biology MCQs
```

## ✏️ How to Update Questions

Each subject has its own JSON file in `data/`. The format is:

```json
{
  "subject": "Modern History",
  "chapters": [
    {
      "chapter_name": "British Expansion in India",
      "questions": [
        {
          "q": "Who was the founder of the British Empire in India?",
          "options": {
            "A": "Lord Minto",
            "B": "Lord Clive",
            "C": "Lord Mayo",
            "D": "C. Sleeman",
            "E": "None of the above"
          },
          "answer": "B",
          "explanation": "Robert Clive was Governor of Bengal from 1757–67...",
          "exam": "BPSC",
          "year": "66th"
        }
      ]
    }
  ]
}
```

**To add/edit questions:** Open the relevant `data/<subject>.json` and edit the questions array. No other file needs to change.

**To add a new chapter:** Add a new object to the `chapters` array inside the subject JSON.

**To add a new subject:** Create a new JSON file in `data/` following the format above, then add an entry to `data/chapters.json`.

## 🚀 Hosting on GitHub Pages

### Step 1 — Create a GitHub Repository

1. Go to [github.com](https://github.com) → **New Repository**
2. Name it `bpsc-quiz` (or anything you like)
3. Set it to **Public** (required for free GitHub Pages)
4. Click **Create Repository**

### Step 2 — Upload Files

**Option A: GitHub Web UI (easiest)**
1. Open your new repository
2. Click **Add file → Upload files**
3. Drag and drop the entire `quiz-site/` folder contents
4. Make sure the folder structure is preserved:
   - `index.html` at the root
   - `css/style.css`
   - `js/app.js`, `js/quiz.js`
   - `data/*.json`
5. Click **Commit changes**

**Option B: Git CLI**
```bash
cd quiz-site
git init
git add .
git commit -m "Initial quiz upload"
git remote add origin https://github.com/YOUR_USERNAME/bpsc-quiz.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. In your repository, go to **Settings → Pages**
2. Under **Source**, select **Deploy from a branch**
3. Choose **main** branch, **/ (root)** folder
4. Click **Save**
5. Wait 1–2 minutes, then visit:
   ```
   https://YOUR_USERNAME.github.io/bpsc-quiz/
   ```

## ⌨️ Keyboard Shortcuts (Quiz Page)

| Key | Action |
|-----|--------|
| `A` / `B` / `C` / `D` / `E` | Select option |
| `Space` | Skip / Check Answer |
| `→` or `Enter` | Next question |
| `←` | Previous question |

## 📊 Question Stats

| Subject | Chapters | Questions |
|---------|----------|-----------|
| Modern History | 10 | 406 |
| Indian Polity | 7 | 203 |
| Biology | 6 | 193 |
| Bihar Special | 3 | 191 |
| Physics | 6 | 188 |
| Indian Economy | 2 | 149 |
| Ancient History | 5 | 128 |
| Mathematics | 6 | 102 |
| World Geography | 2 | 66 |
| **Total** | **47** | **1,626** |

---

*Built for BPSC Prelims preparation. Questions sourced from Priyadarshani Book Series.*
