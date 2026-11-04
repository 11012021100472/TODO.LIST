# Personal OS — Productivity & Knowledge Operating System

A single-user Personal Operating System for tasks, daily execution, clients, learning, knowledge, files, notifications, activity history, backup and recovery.

> Open → Understand → Execute → Record → Learn → Organize → Recover

**Current delivery:** a self-contained interactive HTML prototype, preserved from the supplied project, plus the original BRD and SRS source documents. No build tools, package installation, API keys, or external libraries are required to run the prototype.

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. The prototype is a static client-side demo. Its current sample state is held in browser memory/local storage as implemented in the original prototype.

## Publish with GitHub Pages

1. Create a new GitHub repository.
2. Upload all files and folders from this project (not just `index.html`).
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose branch `main` and folder `/ (root)`, then Save.
6. Wait for the deployment link to appear in the Pages section.

A GitHub Actions workflow is also included at `.github/workflows/pages.yml` for automatic Pages deployment. To use it, set **Settings → Pages → Build and deployment → Source** to **GitHub Actions**.

## Repository structure

```text
personal-os-github/
├── index.html                 # Original interactive HTML prototype
├── docs/
│   ├── BRD.md                 # Original Business Requirements Document
│   └── SRS.md                 # Original Software Requirements Specification
├── .github/
│   └── workflows/
│       └── pages.yml          # GitHub Pages deployment workflow
├── .nojekyll
└── README.md
```

## Product scope preserved from the source documents

The product is intended to evolve through six usable product slices:

1. **MVP-1 — Task Execution:** tasks, subtasks, tags, notes, updates, recurrence, templates, timer and completed history.
2. **MVP-2 — Command Center:** dashboard, quick add, calendar, notifications, reminders, global search and dashboard customization.
3. **MVP-3 — Learning & Knowledge:** courses, categories, progress, notes, knowledge entries, tags, pinning and search.
4. **MVP-4 — Client Workspace:** client profiles/data/status, work history, agreement notes, general notes, custom fields, client tasks/files and export.
5. **MVP-5 — Files & Recovery:** uploads, folders, relationships, previews, trash, restore, activity history, backup, export and storage warnings.
6. **MVP-6 — Offline & Production:** PWA, offline CRUD, sync queue, conflict resolution, push notifications, performance and security hardening.

The original requirements documents remain the authority for detailed behavior, validation, business rules, exclusions, acceptance criteria, release gates and open technical decisions.

## Important implementation status

The included `index.html` is the supplied **prototype**, not a claim that every SRS requirement is already implemented. In particular, production-grade persistence, server-side services, secure backup/restore, file storage, full-text/fuzzy search, push delivery, multi-device synchronization and offline conflict resolution require additional implementation and testing. The prototype's sample data and interactions should not be treated as production data storage.

## Source documents

- `docs/BRD.md` — Business Requirements Document (Arabic)
- `docs/SRS.md` — Software Requirements Specification (Arabic)

These documents are included without rewriting their requirements.
