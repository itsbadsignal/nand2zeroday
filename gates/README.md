# Gate protocol

> How to take a gate alone and have the result mean something.

There is no examiner. The protocol is the examiner, and your public log is the proctor. Every gate in every module is taken under these rules unless the gate says otherwise.

## Before the attempt

1. **Log it first.** Add a row to the attempt log in your fork of [progress.md](../progress.md): gate, attempt number, date, the pool you'll draw from, and the draw method. Commit and push it before you look at the target. The commit timestamp is the start time.
2. **Draw the target, don't browse for it.** See [drawing an unseen target](#drawing-an-unseen-target).
3. **Time it.** Contiguous gates run on a single clock. Cumulative gates log every start and stop in the attempt row.

## Unaided means

Unless a gate says otherwise:

- **Allowed:** the tools the gate names, your own notes, and primary reference documents: man pages, ISA manuals, the language standard, a protocol's RFC or spec.
- **Not allowed:** writeups, forums, other people, and AI assistants. An assistant is an aid like any other.
- **M9 only:** an AI assistant may generate harnesses and navigate code, if every use is logged. Triage is still yours alone.

## Drawing an unseen target

A pool is a list of targets you have never solved, never opened, and never read about. Write the list into the attempt row before the draw. Draw by index: roll dice, or take the first hex digits of `sha256sum` of the date string, modulo the list length. Re-draw only if the target turns out to be one you've seen; log that too.

| Gate | Pool | What the draw picks |
|------|------|---------------------|
| 00a | Khan Academy course challenge; Book of Proof ch. 1 exercises you haven't done | Khan randomises; draw five exercises |
| 00b | A directory you didn't create (an extracted source tarball you haven't opened) | Nothing else to draw |
| M1 | `openssl rand -hex 4`, twice, written down before you look at it closely | The two words |
| M2 | Behaviour claims: the examples on the cppreference [behaviour](https://en.cppreference.com/w/c/language/behavior) page and in the C standard's annex J you haven't studied, rewritten as claims without their category | Five claims |
| M3 | [crackmes.one](https://crackmes.one/) entries you haven't seen, low difficulty, Linux x86-64 | The binary, then the function: number the functions in the listing and draw again |
| M4 | Mitigations: any binary in a package you haven't inspected. Race: [OSTEP](https://pages.cs.wisc.edu/~remzi/OSTEP/) concurrency homework code you haven't run. Protocol: an RFC-specified binary protocol you haven't implemented | One item per part |
| M5 technical | Self-hostable open-source web applications you've never used, deployed in your own lab | The application |
| M5 legal | [The M5 scenario bank](m05-legal-scenarios.md) | Five scenarios |
| M6 | Pwn challenges from past CTFs you didn't play, found through [CTFtime](https://ctftime.org/) event pages, writeups unread. Exclude anything whose name or description names the bug class | The binary |
| M7 parts 2-3 | Same pool as M6, filtered to binaries with mitigations on (check with `checksec` before the draw; that reveals nothing about the bug) | The binary |
| M8 | A function from a binary you built from one of the M4 codebases, CFG dumped by your disassembler. For part 1, a flattened variant you produced with a public obfuscator you didn't configure for that function | The function |
| M9 | None. Target selection is what M9 tests | — |

If a pool runs dry, widen it: a second platform, an older CTF year. Never narrow it to something you've already looked at.

## "Someone else runs it"

M7 fails if the exploit works when you run it and not when someone else does. With nobody else available, "someone else" is a clean machine:

- a container or VM built from a file committed in your repo, on a fresh boot, with ASLR on;
- a run script, committed before the attempt and not edited during it, that executes the exploit the required number of times and logs each result;
- the build file, script and full log published with the writeup.

An interactive run that works on your workstation doesn't count.

## After the attempt

- **Pass or fail, log it.** A failed attempt is published as one line: what you couldn't do. The log is evidence for Rule 1, and for you at the next quarterly look at your pace.
- **Check against the Fail if line only.** Passing is not "close enough". If you're arguing with the Fail if line, you failed.
- **Cold placement attempts** follow the same protocol but don't count toward Rule 1.

## Feedback

You have no mentor, so borrow critique. Publish the attempt writeup and ask for it to be torn apart in the community attached to the resource you used, or by your CTF team. A reviewer can show you what you missed. A reviewer can't pass you: the gate stays self-graded against its Fail if line.
