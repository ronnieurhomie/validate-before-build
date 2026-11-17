# Validate Before Build

A reusable AI skill for pressure-testing hackathon and product ideas before implementation. It helps connect an interesting technical concept to a real user problem, a falsifiable assumption, and a small validation experiment, then recommends **Go**, **Narrow**, or **Pivot**.

Use it when choosing a hackathon idea, adapting an approach from another field, defining an MVP, evaluating a feature proposal, or deciding whether to keep building. The depth should fit the available time: a short hackathon needs credible initial evidence and a feasible demo.

## What it does

1. Clarifies the target user, their task, current workaround, and unmet need.
2. Checks existing products, established methods, and relevant data before claiming novelty.
3. Questions whether a borrowed analogy or measurable proxy supports the real decision.
4. Ranks up to three assumptions whose failure would undermine the idea.
5. Defines a small test, a baseline, and success/failure criteria before observing results.
6. Recommends continuing, narrowing the claim, or changing direction, then scopes the MVP to the evidence.

## Install in Codex

For a personal installation, clone the repository into the user-level skills directory:

```sh
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/ronnieurhomie/validate-before-build.git \
  "$HOME/.agents/skills/validate-before-build"
```

The destination must not already exist. For a project-only installation, use `.agents/skills/validate-before-build` inside that project instead. If the skill does not appear, restart Codex. See [OpenAI's skill documentation](https://learn.chatgpt.com/docs/build-skills) for discovery locations and host-specific behavior.

## Use

In Codex, invoke it explicitly:

```text
Use $validate-before-build to evaluate this hackathon idea before we start coding: [your idea]
```

Include the target user, their current workaround, your proposed approach, available evidence, deadline, and budget when known. Automatic selection is also enabled in the original metadata. In ChatGPT, select an installed skill with `@`; local Codex installation does not install it into your ChatGPT account.

Example prompt (illustrative):

```text
Use $validate-before-build to evaluate a tool that turns long software
release notes into upgrade checklists for solo frontend developers.

We have 36 hours, a $20 budget, public release notes, and no user interviews
yet. Check existing options, identify the riskiest assumptions, and propose
the quickest meaningful test before we choose an MVP.
```

### Expected output

| Part | What you should get |
| --- | --- |
| Verdict | Go / Narrow / Pivot, with a reason |
| Problem and existing approach | Who has the problem, what they do today, and the gap |
| Critical assumptions | Up to three, marked verified, untested, or contradicted |
| Fastest proof | A test, baseline, success/failure threshold, and time estimate |
| MVP if it passes | One core user journey |
| Next action | A concrete step for the user or agent |

Use the proposed test to resolve untested assumptions before committing to a larger build. For a retrospective, the skill identifies where an earlier test could have changed the decision. Read the full workflow in [SKILL.md](SKILL.md).

## Requirements and limits

This is an instruction-based skill, not an executable program. It has no bundled scripts, package dependencies, API credentials, project-data requirements, or dependencies on other skills. It needs a compatible AI host; current-solution research requires browsing or other relevant source access. Domain-specific tests may require task-specific tools or evidence.

Research and experiments consume the time and tool budget of the host and task; this repository does not start services or make API calls by itself. A decision brief is a guide to gathering evidence, not independent proof that a product is useful or a scientific method is valid.

## Files

```text
validate-before-build/
├── .gitignore
├── README.md
├── SKILL.md
├── agents/
│   └── openai.yaml
└── assets/
    └── icon.svg
```

`SKILL.md` contains the workflow and origin lesson. `agents/openai.yaml` preserves its display name, default invocation, product metadata, automatic-invocation policy, and icon references. `assets/icon.svg` supplies both icons.

## Origin and preservation

Created during reflection on the [NASA Space Apps Analog Coverage Gap Map](https://github.com/ronnieurhomie/analog-coverage-gap-map) experience. The project compared lunar and Earth terrain, but similarity alone did not establish practical field-site suitability. The transferable lesson is to validate the link between an available signal and the user's real decision before investing heavily in a larger build. This credits the project experience without implying NASA endorsement.

The three original skill files are preserved byte-for-byte from the ChatGPT Skills export supplied on November 17, 2026. Only this README and `.gitignore` were added for standalone repository packaging. The original workflow, invocation policy, and historical lesson have not been rewritten.

Packaging checks covered the skill's structure, metadata, icon references, and fidelity to the export. They do not establish the skill's effectiveness across products or domains.

## License

No license was included in the original export, and none has been added.
