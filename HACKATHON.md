# Building with IBM Bob: project record

## Current scope

- **Track:** Students / Early Career — Explore, Fix, and Build.
- **Starting application:** `picclaus`, then `cobolinfo` if the team can run the baseline.
- **Upstream:** [jwoehr/ibmi-cobol-examples](https://github.com/jwoehr/ibmi-cobol-examples).
- **Hackathon changes:** None yet. The issue, fix, and feature remain to be chosen after baseline execution.
- **IBM Bob use:** Not yet recorded. Future claims about Bob's contribution must be backed by the team's actual work.

This repository preserves the upstream examples and their commit history. The examples are starting material, not the team's completed hackathon work.

## Preliminary plan (October 9)

1. **Establish access and an unchanged baseline.** Confirm the IBM i host, assigned library, ILE COBOL compiler, PASE `make`, and Bob access. Build and run `picclaus` without changing it. If PUB400 remains unavailable, seek another authorized IBM i environment before claiming runtime results.
2. **Use Bob to understand the application.** Ask Bob focused questions about the DDS screen, COBOL input loop, and how `cobolinfo` extends `picclaus`. Check its answers against source and observed behavior. Save the prompt, useful output, and any human correction.
3. **Select a reproducible issue.** Record expected versus observed behavior, reproduction steps, and a check that fails before the fix. Confirm with organizers what they mean by a "seeded issue" before treating an arbitrary improvement as one.
4. **Fix, then add one bounded feature.** Ask Bob for a scoped proposal, review the diff, compile on IBM i, and exercise the affected 5250 behavior. A faster way to find a clause is one possible feature hypothesis, not a commitment; first confirm the baseline and check that existing `cobolinfo` does not already solve the need.
5. **Prepare the judge path.** Resolve how a 5250 application can satisfy the required live working environment URL. If that cannot be met, choose a project scope that can be demonstrated live before investing in a larger implementation.

The team should ask the October 9 mentor/organizer AMA about the seeded-issue definition and acceptable live-demo access. The event's [submission requirements](https://hackathon.angelhack.com/web/events/building-with-ibm-bob) make both questions consequential.

## Bob workflow and usage evidence

Jack Woehr's [keynote](https://www.youtube.com/watch?v=KyP3dkqWtu0) recommends small, clearly defined tasks and human evaluation of agent output. He describes rules, skills, hooks, and MCP as available ways to customize Bob, not as required project components. Use them only when they solve a concrete problem in this repo.

For each meaningful Bob-assisted change, record: the task and prompt, Bob's proposal, what the team accepted or corrected, the commit, and the observed verification result. This supports the event's 30% Bob-adoption criterion without claiming that upstream code or unaided work was created by Bob.

Check the team's actual Bobcoin balance before substantial sessions and track balance changes after them. IBM's [Bobcoin documentation](https://bob.ibm.com/docs/shell/account/bobcoins) lists 180 monthly coins for a standard Pro+ plan, but that does not establish this team's available balance or hackathon allocation. Keep requests narrow and preserve capacity for debugging and the demo. Do not enable paid overages without a separate decision.

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
