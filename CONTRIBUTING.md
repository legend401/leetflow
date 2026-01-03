# Contributing to LeetFlow

👋 **Welcome!** We love that you want to contribute to LeetFlow. Whether you're fixing a bug, improving the docs, or adding a cool new feature (like LinkedIn support?), we're happy to have you.

## 🚀 Getting Started

### 1. Fork & Clone

Fork the repository to your own GitHub account and then clone it to your local machine:

```bash
git clone https://github.com/davistar21/leetflow.git
cd leetflow
```

### 2. Install Dependencies

This is a monorepo-style setup. The frontend is in `web/`, and scripts are in `scripts/`.

**Frontend:**

```bash
cd web
npm install
```

**Python Scripts:**
Ensure you have Python 3.10+ installed.

```bash
pip install -r scripts/requirements.txt
```

### 3. Environment Setup (Critical!) 🔑

You cannot run the app without API keys.

1.  Copy `.env.example` to `.env` in the **root** directory.
2.  Fill in the keys:
    - **Github Token**: For creating Gists.
    - **Twitter Keys**: Requires "Read and Write" OAuth 1.0a permissions.

> **Note:** If you are just working on the UI, you can mock the API responses or just work on the components in `web/components`.

### 4. Run Locally

Start the Next.js development server:

```bash
cd web
npm run dev
```

Visit http://localhost:3000.

---

## 🏗️ Project Structure

- **`/web`**: Next.js 15 app.
  - `app/`: App Router pages and API routes.
  - `components/`: Shadcn UI components (PascalCase).
  - `lib/`: Utilities and Puter.js integration.
- **`/scripts`**: Python automation.
  - `gist_publisher.py`: Uploads markdown to GitHub Gists.
  - `twitter_poster.py`: Manages threading and posting to X.
  - `progress_tracker.py`: State management (updates `progress.json`).

---

## 🤝 How to Contribute

### Reporting Bugs

- Open an issue on GitHub.
- clearly describe the bug, including steps to reproduce.

### Pull Requests

1.  Create a new branch: `git checkout -b feature/my-cool-feature`.
2.  Make your changes.
3.  **Test your changes!**
    - If modifying UI, check Dark/Light mode.
    - If modifying Scripts, dry-run them.
4.  Commit with descriptive messages.
5.  Push to your fork and submit a Pull Request.

---

## 💡 Ideas for Contribution

- **New Platforms**: Add support for posting to LinkedIn or Dev.to.
- **Better AI**: Improve the prompt in `web/app/page.tsx` for even better storytelling.
- **Themes**: Add more themes/colors to the UI.
- **Tests**: We currently lack a test suite. Adding Jest/Playwright would be legendary.

Happy Coding! 🌊
