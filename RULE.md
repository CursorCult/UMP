---
description: "Simple naming scheme where private entities are prefixed with an underscore"
alwaysApply: true
---

# UNDERSCORE‑MEANS‑PRIVATE Rule (UMP)

The UNDERSCORE‑MEANS‑PRIVATE Rule (UMP) establishes a direct, non‑negotiable contract: any name that begins with `_` is private.

Files, directories, functions, classes, and module‑level symbols all follow the same rule. The leading underscore marks an implementation detail — not part of the public API — and not safe for external callers to rely on. By definition, anything without a leading underscore is public.

UMP removes ambiguity about intended visibility and enforces a clean, testable boundary between stable interfaces and internal mechanics.

## Testing contract

- There should never be any tests directly on UMPs (private entities).
- Private behavior is exercised only through tests of the public surface.
- UMP pairs well with the PUTT PUTT Rule; use both to require total coverage while keeping tests public‑only.

## Visibility boundary

- UMPs should not be used outside of the directory in which they are defined.
- Treat any `_name` as strictly internal to its enclosing unit and directory.
