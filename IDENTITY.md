# Identity

One name, everywhere: **QuantumCoder-14**.

| Where | Value |
| --- | --- |
| GitHub username | `QuantumCoder-14` |
| Display name | `QuantumCoder-14` |
| Commit author name | `QuantumCoder-14` |
| Commit email | `supersiddhantneekhra@gmail.com` (the only verified address on the account) |
| Website | https://quantumcoder-14.github.io |
| Portfolio repo | [quantumcoder-14.github.io](https://github.com/QuantumCoder-14/quantumcoder-14.github.io) |
| Copyright line in licences | Siddhant Neekhra (legal name, licences only) |

The legal name appears only in the copyright line of `LICENSE.md` files. That is
deliberate: a copyright notice should name the person who holds the copyright, while the
handle is the brand people search for.

---

## Set it on a new machine

```bash
git config --global user.name  "QuantumCoder-14"
git config --global user.email "supersiddhantneekhra@gmail.com"
```

Check what a repo will use before committing:

```bash
git config user.name && git config user.email
```

---

## Rules

1. **One handle.** `QuantumCoder-14` on every platform. No older handles, no numbered
   variants.
2. **One commit identity.** `QuantumCoder-14 <supersiddhantneekhra@gmail.com>`.
3. **One website.** https://quantumcoder-14.github.io
4. **Legal name only in licences.** `Siddhant Neekhra` appears in `LICENSE.md` and nowhere
   else, so the two never compete.

---

## The email trap

A commit only links to a GitHub profile if its author email is registered on that account.
`supersiddhantneekhra@gmail.com` is verified there; `sidthehacker07@gmail.com` is not.
Commits authored with an unregistered address still land in the repo, but they are
attributed to nobody — they never appear on the contribution graph or the profile.

To commit from the other address, add it first under **Settings → Emails**, then verify it.

---

## Renaming the commits in history

Some commits predate this file and carry older author names. Rewriting them changes every
commit SHA and requires a force-push, which breaks any other clone you have. Do it once,
deliberately.

```bash
pip install git-filter-repo

git clone https://github.com/QuantumCoder-14/REPO.git
cd REPO
git filter-repo --mailmap ../mailmap.txt --force
git push --force origin main
```

`mailmap.txt`, one line per old identity:

```
QuantumCoder-14 <supersiddhantneekhra@gmail.com> Siddhant........ <supersiddhantneekhra@gmail.com>
QuantumCoder-14 <supersiddhantneekhra@gmail.com> Siddhant Neekhra <sidthehacker07@gmail.com>
```

Repos with old author names, by commit count: SiteRakshak 48, this repo 9, RoadSOS 5,
CrapClean 4, arduinomap 3, Metabatch 1.
