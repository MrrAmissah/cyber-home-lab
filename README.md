# cyber-home-lab

A working record of my hands-on cybersecurity practice: a home lab built as code, one write-up per exercise, and the small tools that come out of it. Everything here runs against systems I own or have written permission to test.

**Who I am:** Prince Kofi Frimpong Amissah, MSc Cybersecurity student at Academic City University, Accra, and founder of PayGuard. GitHub: [MrrAmissah](https://github.com/MrrAmissah).

## What's here

| Folder | Contents |
|---|---|
| `infra/` | The lab itself, as code: VM and container definitions, network layout, baseline configs |
| `labs/` | One folder per exercise: a README write-up, sanitised evidence, and anything needed to reproduce it |
| `docs/` | The network diagram, the write-up template, and the running lab journal |
| `scripts/` | Helper scripts (capture hygiene, secret checks, lab bring-up) |

Related repos: [PacketSage](https://github.com/MrrAmissah/PacketSage) (packet analysis workspace), [SME-IR-Copilot](https://github.com/MrrAmissah/SME-IR-Copilot) (incident-response assistant), [Subnet-Calculator](https://github.com/MrrAmissah/Subnet-Calculator).

## Lab log

Newest first. Each entry links to its write-up.

| Date | Lab | Outcome |
|---|---|---|
| 2026-11 | [00 – Wireshark capture method](labs/00-wireshark-capture-method/) | Clean-capture procedure for TCP handshake and round-trip timing analysis (write-up pending) |

## How each write-up is structured

Every lab README follows [the template](docs/TEMPLATE-writeup.md): **Purpose · Setup · What I did · What I found · What I learned · Limits · How to reproduce.** The "what I learned" and "limits" sections are mandatory; a lab without them isn't finished.

## Ground rules

- **Scope:** only systems I own, or have written authorisation to test. See [SECURITY.md](SECURITY.md).
- **Evidence hygiene:** no real packet captures, credentials, keys, customer data or personal data in this repo. Captures are sanitised before any excerpt is committed; `.gitignore` blocks the raw files and a secrets scan runs on every push.
- **Honesty:** write-ups report what happened, including failures. Negative results are kept.
- **Coursework:** graded university work is not published here until marks are released, and then only as a reworked case study.

## Licence

Code is under the [MIT Licence](LICENSE). Write-ups and diagrams are under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
