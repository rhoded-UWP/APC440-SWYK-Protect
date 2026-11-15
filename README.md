# Break In, Lock It Down

APC 440 Web Development, Module 13 Show What You Know.

A practice copy of the students' Learn Node on Node site with a real SQLite
database running in the browser (sql.js). Students:

1. **Recon: read the query.** See how their input becomes part of the SQL.
2. **The leak.** Use `OR 1=1` on the lesson filter to show unapproved feedback and capture a flag.
3. **The login bypass.** Use `' OR '1'='1' --` on the instructor login and capture a flag.
4. **Lock it down.** Pick the safe version of each handler; the page reruns real attacks against their choice.
5. **Spot the hole.** Judge six Express and pg snippets as safe or unsafe, including AI-written code.

Scores are percents only, so each course can assign its own points. The best
percent per station is kept until the page reloads. Students download a
certificate PNG with a verification code and upload it to Canvas.

## Publish

Settings, then Pages: Deploy from a branch, `main`, folder `/ (root)`.

## Instructor check

Open the published address with `?verify` on the end, type the values from a
certificate, and the page reports MATCH or NO MATCH.

## Files

- `index.html`: the whole activity, no build step
- `learn-node.css`: the Learn Node on Node site styles
- `sql-wasm.js`, `sql-wasm.wasm`: sql.js 1.16.0, kept in the repo so no CDN is needed (MIT license, see `LICENSE-sql.js.txt`)
- `favicon.svg`

Everything runs in the browser. Nothing is sent to a server.
