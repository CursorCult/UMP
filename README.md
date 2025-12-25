# Part of the [CursorCult](https://github.com/CursorCult)

# UMP

The UNDERSCORE‑MEANS‑PRIVATE Rule: any name starting with `_` is private.

**Install**

```sh
pipx install cursorcult
cursorcult link UMP
```

Rule file format reference: https://cursor.com/docs/context/rules#rulemd-file-format

**When to use**

- You want a single, consistent visibility convention across files, symbols, and directories.
- You want to make public APIs explicit and discourage accidental coupling to internals.
- You want tests to operate strictly through public surfaces.

**What it enforces**

- Any name beginning with `_` is private and not part of the public API.
- Anything without a leading underscore is public by definition.
- Private entities are never tested directly; they are exercised through public tests.
- Private entities are not used outside their defining directory.

UMP works especially well with PUTT PUTT: together they enforce public‑only tests and total coverage.

**Credits**

- Developed by Will Wieselquist. Anyone can use it.

**See also**

- PUTT PUTT: https://github.com/CursorCult/PUTTPUTT.git
- UNO: https://github.com/CursorCult/UNO.git
