# Pushing this folder to wizkidproductions

This `website/` folder is part of the UnitySolitaire repo but can be pushed to the **wizkidproductions** GitHub repo so it can be used for GitHub Pages or elsewhere.

## One-time setup (already done)

The remote `wizkid` points to https://github.com/SteveOzipko/wizkidproductions.git

## Push website to wizkidproductions

From the **UnitySolitaire repo root** (one level above this folder), run:

```bash
git subtree push --prefix=website wizkid main
```

- Your Solitaire repo (origin) is unchanged; only the contents of `website/` are pushed.
- The wizkidproductions repo uses the `main` branch. If that repo uses a different default branch (e.g. `master`), change `main` in the command above.

### If push is rejected (“remote contains work that you do not have locally”)

The wizkidproductions repo has a different commit history (unrelated to Solitaire). To **overwrite** it with your current `website/` content (use only if your local site is the source of truth):

```bash
git push wizkid $(git subtree split --prefix=website):main --force
```

Run this from the UnitySolitaire repo root. It replaces `main` on wizkidproductions with the history of your `website/` folder. After this, future pushes can use the normal `git subtree push` command above.

## Pull from wizkidproductions (optional)

If you ever make changes in the wizkidproductions repo and want to bring them back into this folder:

```bash
git subtree pull --prefix=website wizkid main
```

Run both commands from the UnitySolitaire project root, not from inside `website/`.
