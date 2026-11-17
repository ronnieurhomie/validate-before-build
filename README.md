# Validate Before Build

A reusable AI skill for pressure-testing hackathon and product ideas before implementation. It examines the problem, existing solutions, borrowed analogies, risky assumptions, and the cheapest meaningful validation, then recommends **Go**, **Narrow**, or **Pivot**.

## Install and use

After this backup is published to the private GitHub repository, clone it into your Codex skills directory from an account with access:

```sh
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/ronnieurhomie/validate-before-build.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/validate-before-build"
```

The destination must not already exist. Start a new Codex chat after installation, then invoke:

```text
Use $validate-before-build to evaluate this hackathon idea before we start coding: [your idea]
```

Include your target user, available time, and constraints when known. Automatic selection is also enabled in the original metadata. The default output is a concise decision brief with a verdict, problem and existing approach, critical assumptions, validation test, conditional MVP, and next action.

This is an instruction-based skill, not an executable program. It has no bundled scripts, package dependencies, API credentials, project-data requirements, or dependencies on other skills. It needs a compatible AI host; current-solution research requires browsing or other relevant source access. Domain-specific tests may require task-specific tools or evidence.

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

Created during reflection on the **NASA Space Apps Analog Coverage Gap Map** experience: validate the link between an available signal and the user's real decision before investing heavily in a larger build. This credits the project experience without implying NASA endorsement.

The three original skill files are preserved byte-for-byte from the ChatGPT Skills export supplied on November 17, 2026. Only this README and `.gitignore` were added for standalone repository packaging. No license was included in the export, and none has been added.
