# Simple Team Git Workflow

## Before Working

```bash
git pull
```

## While Working

Work on one focused change at a time. Test it, then commit it with a meaningful message.

Good examples:

```text
feat: add combined category filter and price sorting
fix: send session cookie from deployed React client
refactor: separate product card from product list
 docs: document server environment variables
```

Avoid messages such as `update`, `changes`, `final`, or repeated numbered commits.

## After Working

```bash
git status
git add <changed-files>
git commit -m "meaningful message"
git pull --rebase
git push
```

If a conflict occurs, do not delete another member's work. Resolve the conflict together and test the integrated application.

## Submission Version

Record the exact commit:

```bash
git rev-parse HEAD
```

Use this hash in `submission-links.txt`.
