# 06 · The Bug

> Find a memory-corruption bug in something you didn't write, characterise the primitive it yields, and take control of execution. Mitigations stay off, so the mechanism is visible.

**Requires:** [M5 gate](05-the-boundary.md) · **Hours:** 480-700 · **Next:** [M7 · The Defended Target](07-the-defended-target.md)

Mitigations are deliberately off through this module. Turning them on before the mechanism is visible teaches defeat rather than understanding. Stack first; then the heap, which is where most people stall. That is normal and planned for.

## Outcomes

- Reverse a stripped binary to accurate pseudocode.
- Drive a debugger as an instrument, not a crash viewer.
- Recognise every major memory-corruption class on sight.
- Take a crash to instruction-pointer control unaided, and state the primitive precisely: what can be written, where, how many times, under what constraints.

## Resources

| Role | Resource | Cost | Notes |
|------|----------|------|-------|
| Core | [pwn.college · Program Security](https://pwn.college/dojos) | Free | ~95% hands-on, ~160 challenges across five modules. The strongest single resource in the field. The ramp is steep; attrition at the belt boundaries is the gate working. |
| Core | [OST2 · Vulns1001 / Vulns1002: C/C++ vulnerabilities](https://ost2.fyi/Vulns1001) | Free | The bug-class taxonomy taught from the "how do I avoid writing this" direction. |
| Core | [exploit.education · Phoenix](https://exploit.education/phoenix/) | Free | Hand-planted bugs in tiny programs. Use Phoenix, not the deprecated Protostar. |
| Core | [pwntools](https://docs.pwntools.com/) | Free | The scripting standard. |
| Core | [how2heap](https://github.com/shellphish/how2heap) | Free | One technique per directory against pinned glibc versions. The version pinning is the lesson: record your glibc version in every writeup. |
| Core | A small, real, C-heavy open-source project of your own choosing | Free | The Ship needs a bug nobody pointed you at. Start looking at hour one, not hour 450. |
| Core | [Fuzzing101](https://github.com/antonio-morales/Fuzzing101) · exercises 1-2 | Free | Two real CVEs fuzzed with AFL++. Enough to point a fuzzer at your chosen project from the first month. The other eight wait for M9. |
| Core | Source audit drill: in your chosen project or one like it, pick a fixed memory-safety CVE, check out the commit before the fix, and find the bug with source, ASan and a debugger before reading the fix or advisory. Write down where you looked and why, dated, first | Free | ~20 h. The discovery skill the Ship needs, practised where the answer exists to check against. |
| Alt | [HeapLAB pt. 1](https://www.udemy.com/course/linux-heap-exploitation-part-1/) (Kamper) | Varies (Udemy) | Udemy prices are regional and usually discounted; pt. 2 lists at $64.99. Buy on sale. The cheapest high-value buy in the curriculum, if the free heap material stalls. Last updated 2024: check its glibc version against yours. |
| Ref | [ir0nstone · binary exploitation notes](https://ir0nstone.gitbook.io/notes/) | Free | The best free written reference for this material. |
| Ref | [Nightmare](https://guyinatuxedo.github.io/) | Free | 90+ challenges with writeups. Use as an unsticker, not reading material. |
| Ref | *Practical Binary Analysis* (Andriesse, 2018) | ~€50 | Builds your own tooling. |
| Ref | *The Ghidra Book* (Eagle & Nance, 2020) | ~€55 | The methodology holds; the UI doesn't. Written for Ghidra 9.x; current is 12.x (12.2, Oct 2026). |
| Paper | Aleph One, [*Smashing the Stack for Fun and Profit*](https://phrack.org/issues/49/14) (Phrack 49:14, 1996) | Free | The founding document. Read as history and mechanism, not current technique. |
| Paper | [*Once upon a free()*](https://phrack.org/issues/57/9) (Phrack 57:9) · blexim, [*Basic Integer Overflows*](https://phrack.org/issues/60/10) (Phrack 60:10) | Free | The heap and integer-arithmetic origin documents. |
| Practice | [pwn.college · ARM Architecture](https://pwn.college/dojos) (community dojo) | Free | For the ~500 h non-x86 milestone. ARM depth comes in M7. |

Tools (Ghidra, gdb + [pwndbg](https://github.com/pwndbg/pwndbg), pwntools) are the medium and are allowed from day one. Automating a *technique* you haven't performed three times by hand is not.

## Milestones

- **~120 h:** Reverse a stripped binary you haven't seen, with Ghidra, to accurate pseudocode, and mark every unchecked length and copy in it, unaided.
- **~250 h:** Hand-written position-independent shellcode under a bad-character constraint, no framework.
- **~380 h:** Supplied crash → instruction-pointer control, primitive stated precisely.
- **~500 h:** One exploitation challenge solved on a non-x86 architecture.

## Ship

A public writeup of a memory-safety bug **you found** (not one you solved) in a small piece of real open-source software, taken through disclosure to [resolution](../guides/legal-and-lab.md#resolution). If no bug materialises within the module, substitute an independent rediscovery: a fixed memory-safety CVE in real open-source software, found from the pre-fix commit with a dated note of your search written before you read the fix. Treat it as second-best.

## Gate · 8 cumulative hours, logged

Given a binary [drawn](../gates/README.md#drawing-an-unseen-target) with a memory-corruption bug, no source, and no hint as to class or location: locate it, characterise the primitive in precise terms, and demonstrate control of the instruction pointer. Unaided.

**Fail if:** you get IP control but can't characterise the primitive precisely. Characterisation, not the crash, is the skill.

The [web/cloud line](../tracks/README.md#web-cloud-and-logic), open since M5, keeps running alongside this module.
