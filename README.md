# 🧹 gh-action-cleanup-node-modules

Remove all `node_modules` folders from your repository on every push and make sure they are always ignored via `.gitignore`.

Designed for projects where you *never* want to accidentally commit huge `node_modules` folders — even from sub-directories.

---

## 🚀 Features

- Recursively deletes **all** `node_modules/` folders (`find .` based)
- Automatically adds `node_modules/` to `.gitignore` (idempotent)
- Auto-commits the update back to the branch
- Lightweight composite action
- Public, open to contributions 🤝

---

## ⚙️ Usage

In your target repository, create:

```yaml
# .github/workflows/cleanup.yml
name: Cleanup Node Modules

on:
  push:

permissions:
  contents: write

jobs:
  cleanup:
    uses: TheKitoInc/gh-action-cleanup-node-modules@v1
```

---

## 💡 Contributing

PRs welcome!  
Open an issue or submit improvements — especially if you want to ignore other auto-generated folders too (e.g., `dist/`, `.next/`, `.turbo/`, etc.)

---

## 📜 License

MIT
