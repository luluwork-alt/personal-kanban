# 🗂 Personal Kanban Board

A minimal, self-contained Kanban board built with plain HTML, CSS, and JavaScript. No dependencies, no backend, no sign-up — just open and go.

**Live site:** `https://yourusername.github.io/personal-kanban`

---

## ✨ Features

- **Three-column Kanban** — To Do, In Progress, Done
- **Drag & drop** cards between columns
- **Rich task cards** with all the fields you need
- **Monthly auto-export** to Excel — triggers automatically once per month
- **JSON backup & restore** — export/import your data anytime
- **Persistent storage** — data saved in your browser's localStorage
- **Overdue & deadline alerts** — cards highlight when approaching or past due
- **Stats bar** — live count of tasks, overdue items, and blocked tasks
- **Fully offline** — works without an internet connection once loaded

---

## 📋 Task Fields

| Field | Description |
|---|---|
| **Title** | What needs to be done |
| **Description** | Context, details, acceptance criteria |
| **Stakeholder** | Who owns or is affected by this task |
| **Deadline** | Due date with overdue highlighting |
| **Priority** | High / Medium / Low |
| **Effort** | XS / S / M / L / XL |
| **Status Tag** | Blocked · In Review · In QA · Waiting |
| **Tags** | Custom comma-separated labels |
| **Resource Link** | URL to docs, Figma, Jira, etc. |
| **Subtasks** | Checklist with progress bar |
| **Last Updated** | Auto-timestamp on every save |

---

## 🚀 Getting Started

### Option 1 — Open locally
1. Download `index.html`
2. Open it in any browser
3. Start adding tasks — data saves automatically

### Option 2 — Host on GitHub Pages
1. [Create a new repository](https://github.com/new) named `personal-kanban`
2. Set visibility to **Public**
3. Upload `index.html` to the repo root
4. Go to **Settings → Pages → Deploy from branch → main / root**
5. Your board is live at `https://yourusername.github.io/personal-kanban`

---

## 💾 Data & Sync

All data is stored in your **browser's localStorage** — it stays on your device and persists across sessions.

### Syncing across devices
Use the built-in backup buttons in the top-right corner:

| Button | What it does |
|---|---|
| **Export JSON** | Downloads a full backup of all tasks |
| **Import JSON** | Restores tasks from a backup file |
| **Export Excel** | Downloads all tasks as a `.xlsx` spreadsheet |

**Recommended workflow for multi-device use:**
1. Export JSON on Device A
2. Transfer the file (email, iCloud, Google Drive, USB)
3. Import JSON on Device B

### Monthly auto-export
The board automatically downloads an Excel file once per calendar month when you open it (as long as there are tasks). This gives you a running archive of your work without any manual effort.

---

## 📊 Excel Export Format

Each row in the exported `.xlsx` file contains:

`Title · Description · Column · Stakeholder · Deadline · Priority · Effort · Status Tag · Tags · Resource Link · Subtasks · Subtasks Done · Subtasks Total · Created · Last Updated`

You can open this in Microsoft Excel, Google Sheets, or import it into Notion / OneNote for record-keeping.

---

## 🗂 File Structure

```
personal-kanban/
└── index.html      # The entire app — board, styles, and logic
└── README.md       # This file
```

---

## 🛠 Customisation

Everything lives in `index.html`. The design uses CSS variables at the top of the file for easy theming:

```css
:root {
  --bg: #f5f5f3;        /* Page background */
  --surface: #ffffff;   /* Card / panel background */
  --text: #1a1a18;      /* Primary text */
  --muted: #6b6b67;     /* Secondary text */
  --border: #e8e8e5;    /* Borders */
}
```

Change these to retheme the entire board in seconds.

---

## 📌 Tips

- **Drag cards** between columns to update their status
- **Click Edit** (appears on hover) to open the full task editor
- **Overdue tasks** are highlighted in red; tasks due within 3 days show in amber
- **Subtask progress** is shown as a thin bar at the bottom of each card
- Keep your **JSON export** in a cloud folder (iCloud / Google Drive) for a simple manual sync solution

---

## 📄 License

MIT — free to use, modify, and share.
