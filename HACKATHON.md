# Building with IBM Bob: project record

## Current scope

- **Track:** Students / Early Career — Explore, Fix, and Build.
- **Starting application:** `picclaus`, then `cobolinfo` if the team can run the baseline.
- **Upstream:** [jwoehr/ibmi-cobol-examples](https://github.com/jwoehr/ibmi-cobol-examples).
- **Hackathon changes:** None yet. The issue, fix, and feature remain to be chosen after baseline execution.
- **IBM Bob use:** Not yet recorded. Future claims about Bob's contribution must be backed by the team's actual work.

This repository preserves the upstream examples and their commit history. The examples are starting material, not the team's completed hackathon work.

## Baseline build and test

The following procedure comes from the upstream `picclaus` documentation. It has **not yet been executed by this team**.

1. Obtain an IBM i account with ILE COBOL and PASE `make`, and identify an existing library assigned to that account. Do not use `QGPL` on PUB400.
2. Deploy this repository to the IBM i IFS, then enter the `picclaus` directory in a PASE shell.
3. Run `make all LIB=<YOUR_LIBRARY>`, substituting the actual library name.
4. In a 5250 session, run `CALL <YOUR_LIBRARY>/PICCLAUS`.
5. Record the build output and observe the first page, PageDown, PageUp, and F3 behavior. Record failures before changing the source.

The upstream [picclaus README](picclaus/README.md) and [Makefile](picclaus/Makefile) provide the source-specific details. The build requires IBM i and cannot be validated by inspecting the source on Windows.

## Verification record

| Item | Status | Evidence to add |
| --- | --- | --- |
| IBM i login and assigned library | Pending | Password-free session capture and library name |
| Unmodified picclaus build | Pending | Compiler output and created objects |
| Unmodified picclaus run | Pending | 5250 screen capture and key behavior |
| Reproduced issue | Pending | Steps, expected behavior, observed behavior |
| Fix and useful feature | Pending | Commits, Bob contribution, human review, checks |
| Live environment for judges | Pending | Accessible URL and access instructions |

PUB400 was unreachable from this workstation and several external probes on October 9, 2026. This is an environment blocker, not evidence that the example fails to build.

## Submission checklist

- Explain what the team learned about the unfamiliar application.
- Declare only improvements made during the September 28–October 18, 2026 build period.
- Include the reproducible issue, fix, useful feature, and verification evidence.
- Include deployment and testing instructions that judges can follow.
- Add the project description (100 words or fewer), stack, team details, PDF deck, YouTube demo (3 minutes or fewer), and live working environment URL.

The [event page](https://hackathon.angelhack.com/web/events/building-with-ibm-bob) lists the submission requirements and October 18, 2026, 11:59 p.m. EDT deadline. The team should verify its final submission against the event's linked rules before submitting.
