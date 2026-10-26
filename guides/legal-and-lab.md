# Legal scope, lab and disclosure

> Read alongside [M5](../core/05-the-boundary.md). State as of October 2026. This is orientation, not legal advice: read your statute directly, as M5 requires.

## Legal scope

**The standard.** You're authorized when one of four things is true, and you can show it: you own the system; its owner gave you a written authorization; a programme's published scope covers it; or a training platform's published terms invite you onto it (Rule 5). Anything else is unauthorized here, whatever a given court might eventually decide. Missing access control is not permission. Employment is not permission.

**Writing an authorization.** It names: the parties, including someone with authority over the systems; the systems by hostname, address range or asset ID; the dates; the permitted actions; the excluded actions; how data you encounter is handled; and a contact for when something breaks. Signed and dated. Your own lab gets one too (M5 Ship 3): it's practice in writing them.

**UK.** [Computer Misuse Act 1990](https://www.legislation.gov.uk/ukpga/1990/18/contents). There is no research defence. On 7 September 2026, during the Cyber Security and Resilience Bill's committee stage, the Government said it proposes a defence to section 1 for accredited researchers carrying out certain activity. Reporting suggests it would cover little beyond scanning. It is a proposal, not law, and wouldn't cover unaccredited or independent researchers.

**US.** [18 U.S.C. §1030](https://www.law.cornell.edu/uscode/text/18/1030). *Van Buren v. United States* (2021) narrowed "exceeds authorized access". In May 2022 the DOJ revised its charging policy to say good-faith security research should not be charged under the CFAA. That is prosecutorial policy, not statute: it can change, it doesn't bind states, and it doesn't stop civil suits. Confirm it's still in force before relying on it.

**EU.** Each member state has its own offences, implementing the [Budapest Convention](https://www.coe.int/en/web/conventions/full-list?module=treaty-detail&treatynum=185) and Directive 2013/40/EU on attacks against information systems. A few states have added protections for researchers; most haven't. Read your national law.

**What changed on the vendor side.** NIS2 (Article 12) requires each member state to name a CSIRT as coordinator for vulnerability disclosure, and ENISA runs the [European Vulnerability Database](https://www.enisa.europa.eu/news/consult-the-european-vulnerability-database-to-enhance-your-digital-security). From 11 September 2026 the [Cyber Resilience Act](https://digital-strategy.ec.europa.eu/en/policies/cra-reporting) requires manufacturers to report actively exploited vulnerabilities to ENISA within 24 hours. These bind vendors and states, not you. They give you a coordinator to go to when a vendor won't answer, and they change how fast EU vendors move once your report says "exploited".

## Lab rules

1. **Isolated by default.** Targets live on a host-only or internal network. No bridged adapter on a target VM, ever.
2. **Built from a script.** Every lab machine comes from a committed file (Vagrant, Ansible, a Dockerfile). If you can't rebuild it identically, it isn't a lab.
3. **Snapshot before, destroy after.** Snapshot before each session; roll back or destroy when you're done.
4. **Nothing untrusted on the host.** Challenge binaries, samples and crash inputs run inside the lab only.
5. **No real data.** No real credentials, personal data or work material in the lab. Never put an employer's or client's data in it.
6. **Authorization on file.** A dated written authorization for your own lab, kept with the lab's scripts.

## Disclosure

The [CERT Guide to Coordinated Vulnerability Disclosure](https://certcc.github.io/CERT-Guide-to-CVD/) is the reference; this is the path through it.

1. **Confirm** the bug on your own copy. Reduce it to a minimal reproducer.
2. **Stop at proof.** Demonstrate impact without accessing more data or systems than the proof needs.
3. **Find the channel:** the vendor's security policy, a `security.txt` file (RFC 9116), the project's advisory process, or the programme's platform. If there's none, your national CSIRT coordinator.
4. **Report** with: affected versions, reproducer, impact, and your disclosure deadline. Keep every message.
5. **Track the timeline** in a public-ready log: report, acknowledgement, fix, advisory.
6. **Publish** after resolution, with the timeline.

**Deadline.** Default to 90 days from report, with a short extension if a fix is close and the vendor asks. That is the norm set by large research teams such as Project Zero, not a law. Agree changes in writing.

**CVE.** If the vendor is a CVE Numbering Authority, they assign it. Otherwise request one through a CNA whose scope covers the product, such as GitHub for projects that publish advisories there.

**Never:** demand payment as a condition of not publishing; publish before the deadline without the vendor's agreement; keep data you encountered; test further to "improve" a finding after reporting it, unless the vendor asks.

### Resolution

M6 Ship, M7 Ship 2 and the M9 gate require disclosure "to resolution". Resolution is any one of:

1. the vendor ships a fix or publishes an advisory;
2. the vendor declines in writing, or a programme closes the report as valid but won't fix (a duplicate of a valid report counts for M7);
3. your stated deadline passes with no fix, and you publish per the steps above, having told the vendor first.

Vendor silence can't hold a gate open past your deadline. Your conduct is what's graded: a report the vendor ignores still resolves.
