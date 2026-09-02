# SQL Formatter

Format and minify SQL in the browser. Clause-aware line breaks, indented subqueries, keyword casing, and a token-preserving formatter that never rewrites your literals.

**Live:** <https://sql-formatter.slippylabs.com/>

## What it does

- Clause-aware layout — major clauses on their own lines, subqueries indented.
- Keyword casing to upper, lower, or left exactly as you typed it.
- Indent with 2 spaces, 4 spaces or a tab; or minify the query back down.

## How it works

The formatter tokenises first and reassembles from tokens, so **string literals, quoted identifiers and comments are never rewritten** — a keyword sitting inside `'a select statement'` stays lowercase, and a `--` comment keeps its text and its line. Formatters that work by regex over raw text get this wrong, and it corrupts queries quietly.

## Run it locally

A static site. No build step, no package manager, no dependencies:

```
git clone git@github.com:slippylabs/sql-formatter.slippylabs.com.git
cd sql-formatter.slippylabs.com
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

---

Part of [Slippy Labs](https://slippylabs.com). Every tool is indexed at
[projects.slippylabs.com](https://projects.slippylabs.com).
