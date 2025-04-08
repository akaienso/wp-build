# 🛠 wp-build

**wp-build** is a lightweight Bash utility for packaging and versioning WordPress plugins or themes using Git tags and semantic versioning.

---

## 🚀 Features

- Detects plugin or theme automatically from standard file structure
- Extracts version from plugin header or style.css
- Builds installable `.zip` archives in organized release directories
- Auto-increments pre-release versions (`--alpha`, `--beta`, `--rc`, `--test`)
- Supports manual override of tags via `--tag-name`
- Dry-run mode to preview actions without writing to disk or Git

---

## ⚙️ Usage

```bash
wp-build                  # Package plugin automatically
wp-build --theme          # Package theme (requires style.css)
wp-build --beta           # Auto-increment beta tag like v1.2.3-beta.2
wp-build --rc             # Auto-increment RC release
wp-build --final          # Final release, no Git tag created
wp-build --tag-name=v1.2.3-alpha.5   # Use explicit tag
wp-build --dry-run        # Preview without writing
```

---

## 📁 Output Structure

Archives are created in a structured release folder:

```text
../releases/
└── beta/
    └── 1.2.3-beta.3/
        └── your-plugin.zip
```

---

## 📦 Requirements

- Git
- Bash (Linux, macOS, or WSL)
- Proper WordPress plugin or theme header

---

## 👤 Author

Created by [Rob Moore](https://github.com/akaienso) 

If you have suggestions, feedback, or want to contribute, feel free to open an issue or PR.

## 📝 License

MIT License — use freely, contribute back if you'd like!
