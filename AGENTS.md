# Repository Guidelines

## Project Structure & Module Organization

- Entry: `index.html` (root) — the current site entry point.
- Add static assets under `assets/` or `static/`; scripts under `js/`, styles under `css/`.
- If introducing a build step, use `src/` for sources and `dist/` for build output.

## Build, Test, and Development Commands

- Local preview (no build): `python -m http.server 8000` — serves the repo at `http://localhost:8000`.
- Quick open: `open index.html` (macOS) or double-click the file in your file manager.
- If a Node toolchain is added: `npm install`, `npm run build`, `npm test`.
- Formatting (when configured): `npx prettier --write .`.

## Coding Style & Naming Conventions

- Indentation: 2 spaces for HTML/CSS/JS.
- Filenames and folders: `kebab-case` (e.g. `css/main.css`, `js/app.js`).
- JavaScript: `camelCase` for variables, `PascalCase` for components.
- Environment/config keys: `UPPER_SNAKE_CASE` in `.env` files.
- Use Prettier and ESLint if present; include an `.editorconfig` for editor consistency.

## Testing Guidelines

- No testing framework is included currently. When added:
  - Place tests under `tests/` or `__tests__/`.
  - Test files: `module.test.js` or `module.spec.js`.
  - Run tests with `npm test` or `pytest`, depending on the stack.
- Prefer small, fast unit tests and a few integration checks for UI changes.

## Commit & Pull Request Guidelines

- Follow Conventional Commits: `feat:`, `fix:`, `docs:`, `chore:`.
- PRs should include a short description, linked issue (if any), steps to reproduce, and screenshots for UI changes.
- Keep PRs focused; rebase or squash commits when requested by maintainers.

## Security & Configuration Tips

- Never commit secrets. Use `.env` and add secrets to `.gitignore`.
- Provide `config.example` or `env.example` for non-sensitive defaults.

If unclear, open an issue describing the change and tag a maintainer for guidance.

