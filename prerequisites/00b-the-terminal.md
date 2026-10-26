# 00b · The Terminal

> Own the machine you already have: shell, editor, version control, one scripting language, and a Linux install of your own.

**Requires:** a computer · **Hours:** 40-80** from zero; 30-50 if you already use a terminal · **Next:** [M1 · The Machine](../core/01-the-machine.md), with [00a](00a-the-numbers.md)

Runs in parallel with [00a · The Numbers](00a-the-numbers.md). Both gates open M1.

## Outcomes

- Navigate and manipulate a filesystem from a shell without hesitating.
- Use one editor competently.
- Commit, branch, push and read a diff.
- Automate a chore you actually have, in Python.
- Install Linux in a virtual machine, snapshot it, break it, restore it.

## Resources

| Role | Resource | Cost | Notes |
|------|----------|------|-------|
| Core | [pwn.college · Linux Luminarium](https://pwn.college/dojos) | Free | Browser workspace, nothing to install. Teaches the shell as adversarial territory. |
| Core | [MIT · The Missing Semester](https://missing.csail.mit.edu/) | Free | Shell, editors, tooling, debugging, git. Assumes you've met a terminal: do it after Luminarium, not alongside. |
| Core | [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/) | Free | Through functions and file I/O. pwntools, fuzzers and angr all assume Python. |
| Alt | [OverTheWire · Bandit](https://overthewire.org/wargames/bandit/) | Free | Gentler than Luminarium, less thorough. |
| Alt | [The Linux Command Line](https://linuxcommand.org/tlcl.php) (Shotts) | Free | If you prefer a book. |
| Ref | [Pro Git](https://git-scm.com/book/en/v2) | Free | Chapters 1-3. |

## Milestones

- **~15 h:** In one pipeline, written from memory: find every file over 10 MB modified in the last week, sort by size, write to a file.
- **~40 h:** A Linux VM you installed yourself, with a snapshot you've restored from at least once. M2 onward runs there.

## Ship

A public repo with a script that automates something you were doing by hand, plus a README explaining what it does and why.

## Gate · 2 hours

1. From a directory of mixed files, produce a shell-only report: counts by type, the ten largest, and any containing a given string.
2. Clone a repo, branch, commit with a meaningful message, and explain what a merge conflict is and how you'd resolve it.
3. Write a script that takes a filename argument, handles a missing file, and produces useful output.

**Fail if:** you look up basic navigation, or the script crashes on a missing file.
