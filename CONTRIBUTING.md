# Contributing to CCNA Practice Labs

Thanks for your interest in contributing! Here's how to do it properly.

## How to Contribute

1. **Fork** this repository
2. Create a new branch: `git checkout -b fix/lab-04-typo`
3. Make your changes
4. Test your changes (verify configs work in Packet Tracer)
5. Commit with a clear message: `git commit -m "Fix: Lab 04 VLAN assignment typo"`
6. Push to your fork: `git push origin fix/lab-04-typo`
7. Open a **Pull Request** against `main`

## What You Can Contribute

- ✅ Fix typos or errors in lab instructions
- ✅ Improve explanations or hints
- ✅ Add Packet Tracer (.pkt) topology files
- ✅ Add alternative solutions to `solution.md`
- ✅ Improve the auto-grader checks in `index.html`
- ✅ Translate labs to other languages (in a separate folder)

## What NOT to Do

- ❌ Do not push directly to `main` — always use a Pull Request
- ❌ Do not add external JavaScript or CDN dependencies to the grader
- ❌ Do not commit credentials, API keys, or personal information
- ❌ Do not delete or restructure existing labs without discussion first
- ❌ Do not add copyrighted Cisco material

## Branch Naming Convention

- `fix/` — bug fixes or typos (e.g., `fix/lab-12-ospf-typo`)
- `feat/` — new features (e.g., `feat/add-pkt-files`)
- `docs/` — documentation improvements (e.g., `docs/improve-readme`)

## Code of Conduct

Be respectful, constructive, and helpful. This is an educational project meant to help people learn networking.

## Questions?

Open an **Issue** if you have questions or suggestions before starting work.