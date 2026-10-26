# M5 legal gate: scenario bank

> Draw five. For each, answer: authorized or not, and the basis (a document, a programme scope, a statute, or ownership). Then check against the [key](keys/m05-legal-key.md), and not before.

Draw under the [gate protocol](README.md#drawing-an-unseen-target). Answer in writing. "Probably fine" fails the gate; so does an answer with no basis. Where the answer depends on a document, quote the clause that decides it.

1. You rent a virtual server. The provider's acceptable-use policy says: "Customers may security-test their own instances without prior approval." You port-scan your instance.
2. A bounty programme lists `*.shop.example` in scope and `payments.shop.example` out of scope. You test `payments.shop.example`.
3. Same programme. You find `legacy.shop.example`, covered by the wildcard. It resolves to a third-party SaaS provider. The policy says: "Assets hosted by third parties are out of scope."
4. A friend who works as a developer at a company messages you: "Go ahead, test our website." He doesn't own the company and has no role in security.
5. You read the source of an open-source library, build it in your own lab VM, and crash it with crafted input.
6. Having found that crash, you send the same input to a public website you know uses the library, "just to confirm".
7. You attack a challenge instance pwn.college started for you.
8. During in-scope testing you reach a database of customer records. The policy says: "If you access personal data, stop and report." You download the full table to prove impact.
9. You work in a SOC. A client's tenant is in your employer's contract, but not in any ticket assigned to you. You run a vulnerability scanner against it to "get ahead".
10. A vendor's disclosure page says: "We welcome reports of vulnerabilities you discover." It says nothing about testing. You test their production login for missing rate limits.
11. You buy an IP camera, dump its firmware and fuzz its web interface on your home network. Its licence forbids reverse engineering.
12. During a CTF, you attack the scoreboard server. The rules list challenge hosts only.
13. An open Wi-Fi network in your building has no password. You join it and scan the other hosts.
14. A search engine for exposed services lists a company database with no password. You query it to see what's inside.
15. A programme's authorization letter covers testing until 30 November. You test on 2 December, finishing what you started.

Add your own scenarios to the bank only after you've passed the gate, and write their key entries at the same time.
