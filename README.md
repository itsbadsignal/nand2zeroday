<div align="center">

# Nand2ZeroDay
**Open Security Vulnerability Research™**

`from zero` · `to original research` · `~4,000h core` · `free-first`

</div>

A self-paced, dependency-ordered path from no computer science background to finding, exploiting and disclosing vulnerabilities nobody handed you.
It required no degree: your published work is the credential.

## Principles

1. **Competence over attitude.** You leave a module by passing its gate. Reading the material doesn't count.
2. **Build before you break.** You write a network service before attacking protocols, implement crypto before breaking it, and build an interpreter before attacking a JIT.
3. **Read code and write code.** Assembly at reading fluency is a foundation, not a specialism.
4. **Theory separates researchers from technicians.** Finding a *new* bug class takes knowing where the machinery's assumptions fail.
5. **Your public work is the credential.** Writeups, exploits, patches and advisories count for more than certifications.
6. **Authorization is the boundary, and it is written down.** No skill level makes the document stop mattering.

## Curriculum
**Prerequisites**
- [[#]]

### Prerequisites
#### M00 - The Terminal
> Own the machine you already have: shell, editor, version control, one scripting language, and the math floor.

**Requires:** a computer · **Hours:** 30-50** · **Next:** []

##### Outcomes
- Navigate and manipulate a filesystem from a shell without hesitating.
- Use one editor competently.
- Commit, branch, push and read a diff.
- Automate a chore you actually have, in Python.
- Read basic mathematical notation (Σ, ∈, ⊆, f(x)) and work with exponents and logarithms.

##### Resources
| Role | Resource | Cost | Notes |
|------|----------|------|-------|
| Core | [pwn.college · Linux Luminarium](https://pwn.college/dojos) | Free | Browser workspace, nothing to install. Teaches the shell as adversarial territory. |
| Core | [MIT · The Missing Semester](https://missing.csail.mit.edu/) | Free | Shell, editors, tooling, debugging, git. |
| Core | [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/) | Free | Through functions and file I/O. pwntools, fuzzers and angr all assume Python. |
| Alt | [OverTheWire · Bandit](https://overthewire.org/wargames/bandit/) | Free | Gentler than Luminarium, less thorough. |
| Alt | [The Linux Command Line](https://linuxcommand.org/tlcl.php) (Shotts) | Free | If you prefer a book. |
| Ref | [Pro Git](https://git-scm.com/book/en/v2) | Free | Chapters 1-3. |
| Ref | [Khan Academy · Algebra](https://www.khanacademy.org/math/algebra) · [Book of Proof](https://richardhammack.github.io/BookOfProof/) ch.1 | Free | Math floor. If Book of Proof ch.1 reads fine, you're past it. |

Calculus, linear algebra and statistics aren't needed. Only the RF track needs calculus.

##### Milestones
- **~15 h:** In one pipeline, written from memory: find every file over 10 MB modified in the last week, sort by size, write to a file.

##### Ship
A public repo with a script that automates something you were doing by hand, plus a README explaining what it does and why.

##### Gate · 2 hours
1. From a directory of mixed files, produce a shell-only report: counts by type, the ten largest, and any containing a given string.
2. Clone a repo, branch, commit with a meaningful message, and explain what a merge conflict is and how you'd resolve it.
3. Write a script that takes a filename argument, handles a missing file, and produces useful output.

**Fail if:** you look up basic navigation, or the script crashes on a missing file.



### Core

#### M01 · The Machine
> Understand what a computer physically does, from a single logic gate up to a CPU.

#### M02 · The Program
> C properly, the process as a laid-out address space, and the discrete math everything after M8 rests on.


#### M03 · The Instruction Stream
> Read x86-64 fluently, without a decompiler.


#### M04 · The System
> Descend to the syscall boundary until the loader, the kernel and the wire are all visible at once.


#### M05 · The Boundary
> Learn what a trust boundary is in access control, cryptography, the web, the cloud and the law before crossing one.


#### M06 · The Bug
> Find a memory-corruption bug in something you didn't write, characterise the primitive it yields, and take control of execution. Mitigations stay off, so the mechanism is visible.


#### M07 · The Defended Target
> Everything from M6, against targets that fight back: mitigations on, reliability required, two architectures, the bug no longer handed to you.


#### M08 · The Theory
> Automata, compilers, dataflow and static analysis, at the depth research consumes, placed where it is finally motivated.


#### M09 · The Research
> Stop being handed bugs.


### Tracks
#### M10 -