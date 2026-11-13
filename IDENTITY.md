# Identity

One name, everywhere: **S-procoder**.

| Where | Value |
| --- | --- |
| GitHub username | `S-procoder` |
| Display name | `S-procoder` |
| Commit author name | `S-procoder` |
| Commit email | `supersiddhantneekhra@gmail.com` (the only verified one on the account) |
| Website | https://s-procoder.github.io |
| Copyright line in licences | Siddhant Neekhra (legal name, licences only) |

---

## Set it on a new machine

```bash
git config --global user.name  "S-procoder"
git config --global user.email "supersiddhantneekhra@gmail.com"
```

A commit only links to the profile if its author email is registered on the account.
`supersiddhantneekhra@gmail.com` is verified there. `sidthehacker07@gmail.com` is not, so
commits authored with it are attributed to nobody and never appear on the contribution
graph. Add it under **Settings → Emails** if you want to keep using it.

---

## The old name, and where it still lives

The account was renamed once, to `S-procoder`. The previous login is deliberately not
repeated in this file, or anywhere else in these repositories — a full sweep of all twelve
repos, private ones included, found zero occurrences. It survives in three places outside
the files:

| Where | What it does | Fix |
| --- | --- | --- |
| The git credential on this machine | Authenticates under the account's previous login, which GitHub no longer accepts for writes, so every `git push` returns **403** | Disconnect and reconnect the GitHub integration, or push from a machine signed in as `S-procoder` |
| `SiteRakshak` → Settings → Collaborators | A stale collaborator entry under the previous login — it is the same account, so it is harmless | Remove only if you are certain; it is an access entry on a private repo |
| Commit author names in history | `Siddhant........` on about 66 commits across six repos | History rewrite, below |

Nothing is broken by the first two. The third is cosmetic.

---

## Renaming the commits in history

This changes every commit SHA in the affected repos and requires a force-push, so it will
break any other clone you have. Do it once, deliberately.

```bash
# install once
pip install git-filter-repo

# per repo
git clone https://github.com/S-procoder/REPO.git
cd REPO
git filter-repo --mailmap ../mailmap.txt --force
git push --force origin main
```

`mailmap.txt`, one line per old identity:

```
S-procoder <supersiddhantneekhra@gmail.com> Siddhant........ <supersiddhantneekhra@gmail.com>
S-procoder <supersiddhantneekhra@gmail.com> S-procoder <supersiddhantneekhra@gmail.com>
S-procoder <supersiddhantneekhra@gmail.com> Siddhant Neekhra <sidthehacker07@gmail.com>
```

Repos affected, by commit count: SiteRakshak 48, S-procoder 9, RoadSOS 5, CrapClean 4,
arduinomap 3, Metabatch 1.

Force-pushing needs the credential problem above fixed first. Until then, no history
rewrite is possible from here — the API cannot change existing commits, only add new ones.
