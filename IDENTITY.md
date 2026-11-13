# Identity

One name, everywhere: **S-procoder**.

| Where | Value |
| --- | --- |
| GitHub username | `S-procoder` |
| Display name | `S-procoder` |
| Commit author name | `S-procoder` |
| Commit email | `supersiddhantneekhra@gmail.com` |
| Website | https://s-procoder.github.io |
| Portfolio repo | [s-procoder.github.io](https://github.com/S-procoder/s-procoder.github.io) |

The only place the legal name appears is the copyright line inside `LICENSE.md` files —
**Siddhant Neekhra**. That is deliberate: a copyright notice should name the person who
holds the copyright, while the handle is the brand people search for.

---

## Set it on a new machine

```bash
git config --global user.name  "S-procoder"
git config --global user.email "supersiddhantneekhra@gmail.com"
```

Check what a repo will use before committing:

```bash
git config user.name && git config user.email
```

---

## Rules

1. **One handle.** `S-procoder` on every platform. No second identity, no `QuantumCoder7`,
   no numbered variants.
2. **One commit identity.** `S-procoder <supersiddhantneekhra@gmail.com>`.
3. **One website.** https://s-procoder.github.io
4. **Legal name only in licences.** `Siddhant Neekhra` appears in `LICENSE.md` and nowhere
   else, so the two never compete.

---

## The email trap, and why it matters

A commit only links to a GitHub profile if its author email is **registered on that
account**. `supersiddhantneekhra@gmail.com` is verified there; `sidthehacker07@gmail.com`
is not. Commits authored with an unregistered address still appear in the repo, but they
are attributed to nobody — they do not count on the contribution graph and do not show on
the profile.

If you want to commit from the other address, add it first:
**GitHub → Settings → Emails → Add email address**, then verify it. Until then, use the
primary one.

---

## Historical drift

Some older commits were authored under other names, from before this file existed:

| Name used | Where |
| --- | --- |
| `Siddhant........` | SiteRakshak (48), S-procoder (3), Metabatch, CrapClean, arduinomap |
| `Siddhant Neekhra <sidthehacker07@gmail.com>` | commits made during the Nov 2026 build-out |
| `S-procoder <supersiddhantneekhra@gmail.com>` | original repo setup |

Rewriting that history would unify the display, but it changes every commit SHA and breaks
any existing clone. Left as-is unless there is a reason to do it.
