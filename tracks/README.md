# M10 · Tracks

> One or two specialisations, past the published edge.

**Requires:** [M9 gate](../core/09-the-research.md), except the web/cloud line (M5 gate) · **Hours:** 600+ each

Choose on evidence of where you are strongest, and choose at most two. Evidence means your gate logs and shipped work, not interest.

## Every track exits the same way

**Ship:** original work in the track's domain that a practitioner would cite: a variant family found from one bug, a tool with documented independent adoption, or a published paper or talk.

**Gate:** two previously unknown defects in the track's domain, in targets you selected on your own reasoning, each with a dated selection note and each carried to [resolution](../guides/legal-and-lab.md#resolution).

**Fail if:** both findings are the same bug in the same component.

## Web, cloud and logic

The one line that opens before M9. It runs in parallel with M6-M7 once the [M5 gate](../core/05-the-boundary.md) is passed, and becomes a full track after M9.

**Rules while it runs alongside the core:**

- At most 20% of weekly hours until the M7 gate. The memory-corruption spine is the path; this line is the income and the feedback loop.
- In-scope bug bounty work only, under each programme's written policy, read in full before the first request.
- Every submission, valid or not, goes in the ship log.

**Checkpoint at M7.** [M7](../core/07-the-defended-target.md) Ship 2 (one valid bounty finding to resolution) is this line's checkpoint. Someone who stops at M7 with this line behind them has a complete application-security and offensive-engineering profile.

| Role | Resource | Cost | Notes |
|------|----------|------|-------|
| Core | [PortSwigger Web Security Academy](https://portswigger.net/web-security) | Free | Finish every topic, including the expert labs. It trains recognition; the programmes train discovery. |
| Core | [flaws.cloud](https://flaws.cloud/) · [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat) | Free | Carried from M5. Every CloudGoat scenario, deployed by you. |
| Core | Bug bounty programmes on [HackerOne](https://hackerone.com/directory/programs) and [Bugcrowd](https://bugcrowd.com/programs) with explicit safe harbour | Free | Pick one programme and stay with it for a month before moving on. Depth on one target finds logic bugs; breadth finds duplicates. |
| Ref | [MDN · Web security](https://developer.mozilla.org/en-US/docs/Web/Security) | Free | Same-origin, CORS, CSP, cookies. |
| Ref | [CERT Guide to Coordinated Vulnerability Disclosure](https://certcc.github.io/CERT-Guide-to-CVD/) | Free | For findings outside a programme. |

### Milestones

- **~100 h:** All PortSwigger apprentice and practitioner labs done.
- **~250 h:** First submission to a programme, valid or not, written up.
- **~400 h:** An authorization or logic flaw found on a programme without a lab or writeup pointing at its class.

## Symbolic execution and program analysis

**Requires:** M9 gate, with the [M8](../core/08-the-theory.md) theory fresh.

| Role | Resource | Cost | Notes |
|------|----------|------|-------|
| Core | [angr](https://docs.angr.io/) · [OST2 RE3201: Symbolic Analysis](https://ost2.fyi/RE3201) | Free | Carried from M9, now to the engine's internals. |
| Core | [Static Program Analysis](https://cs.au.dk/~amoeller/spa/) (Møller & Schwartzbach) · the chapters M8 skipped | Free | Pointer analysis, interprocedural analysis, abstract interpretation in full. |
| Core | [GitHub Security Lab · CodeQL](https://codeql.github.com/) | Free | Query packs as research output. |
| Core | [LLVM · writing a pass](https://llvm.org/docs/WritingAnLLVMNewPMPass.html) | Free | Instrumentation for your own analysis. |
| Alt | *Introduction to the Theory of Computation* (Sipser, 3rd ed.) | ~€70 | Now the complexity-theory back half too: it's why your solver times out. |

## RF

> **Draft.** Not written. This is the one track that needs calculus. No resource is listed until one is verified.

## Candidate tracks

Not written yet. Each becomes a track once it has a verified resource path and a gate. What the core already gives each:

| Candidate | Core foundation |
|-----------|-----------------|
| Kernels | M4 xv6 labs; pwn.college Software Exploitation's kernel module (M7) |
| Browsers and JITs | M8 Crafting Interpreters; M7 mitigations |
| Hypervisors | M4 paging and traps; 6.5660 isolation (M5) |
| Mobile | M7 ARM64, PAC, MTE and Apple MIE |
| Firmware and embedded | M7 ARM; M4 binary formats |
| Memory-safe-language targets: Rust `unsafe`, logic and type-confusion bugs in managed runtimes, data races in Go | M9 auditing; M8 analysis; M4 concurrency |
