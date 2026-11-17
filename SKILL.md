---
name: validate-before-build
description: Pressure-test hackathon concepts, AI product ideas, prototypes, and feature proposals before implementation. Use when brainstorming, selecting a challenge, adapting inspiration from another domain, defining an MVP, planning a hackathon, or deciding whether to continue building. Establish the real problem, existing solutions, falsifiable assumptions, and a fast validation plan before coding.
---

# Validate Before Build

Help the user move from an interesting concept to a defensible, testable solution quickly. Be constructively skeptical without killing creative exploration. For time-boxed hackathons, prioritize a feasible demonstration and honest evidence over research-grade validation.

## Workflow

### 1. Name the problem independently of the solution

Specify the target user, their concrete task, current workaround, specific friction, and why it matters. Separate observed facts from assumptions. Ask no more than three high-leverage clarification questions when necessary; otherwise state assumptions and proceed.

### 2. Check existing solutions before claiming novelty

Research current products, established scientific/industry methods, and available datasets where relevant. Use authoritative sources for technical claims. Identify the actual improvement opportunity: accuracy, access, cost, speed, usability, coverage, or new workflow. If the user's idea already exists, say so and assess a meaningful extension.

### 3. Challenge borrowed analogies

When inspired by another case, distinguish the transferable mechanism from its domain-specific evidence. Ask:

- Are we detecting an object/anomaly, predicting an outcome, or recommending an action?
- Does the data measure the thing that determines real-world success, or merely a proxy?
- What additional causal link must hold for a pattern match to become a useful decision?
- What ground truth or independent verification exists?

Do not carry over another project's success claims without checking its evidence and validation.

### 4. Find the riskiest assumptions

List at most three, ranked by how completely failure would invalidate the idea. Distinguish desirability (the user wants it), feasibility (it can be built), and validity/usefulness (outputs are meaningfully correct). State what would falsify each assumption.

### 5. Design the cheapest decisive test

Before a polished UI, specify:

- **Baseline:** current practice, random selection, simple heuristic, or a known example.
- **Test:** smallest manual or coded experiment with representative cases.
- **Success criterion:** observable metric and a threshold chosen *before* seeing results.
- **Failure criterion:** what result triggers a pivot or a narrower claim.
- **Data limits:** sampling, leakage, resolution, missing variables, and independence.

Match rigor to context: usability tests for interactive products, task success/time for agents, learning checks for education, held-out benchmarks for prediction, and domain-expert/field checks when physical suitability is claimed. For a hackathon, a modest credible test is better than an elaborate untested model.

### 6. Make a go / narrow / pivot recommendation

- **Go:** key assumption has enough initial support; build the smallest useful flow.
- **Narrow:** data supports exploration or prioritization but not definitive recommendations; change wording and MVP scope.
- **Pivot:** core assumption fails and the project cannot deliver credible value in available time.

Do not equate a working UI with a validated solution. Do not call an unmet benchmark a success. Failed tests are evidence and should change the claim or direction.

### 7. Build and communicate only what the evidence supports

Map each claimed benefit to a demo interaction and an observed result. Clearly distinguish **observed finding**, **interpretation**, **intended impact**, and **unverified assumption**. Never invent metrics. For short deadlines, stop adding features once evidence, a stable demo, and submission requirements are secured.

## Default response format

Give a concise decision brief:

1. **Verdict:** Go / Narrow / Pivot, with one reason.
2. **Problem & existing approach:** Who suffers, what they do now, and the gap.
3. **Three critical assumptions:** Mark verified, untested, or contradicted.
4. **Fastest proof:** Test, baseline, success/failure threshold, time estimate.
5. **MVP if it passes:** One core user journey, not a feature list.
6. **Next action:** What the user or agent should do immediately.

If the user asks to start implementation, complete the critical test first when practical, then proceed based on the result. For a retrospective, identify where an early test could have changed the decision and extract one transferable process rule; do not retroactively claim the whole idea was worthless.

## Lesson behind this skill

In the Analog Coverage Gap Map NASA Space Apps project, comparing lunar and Earth elevation data produced inspectable candidates, but two retrieval tests failed and a third was inconclusive. The key mistake was treating **terrain-shape similarity** as a path to **field-site suitability** before proving the matching method and its decision relevance. The transferable lesson: validate the bridge between the available signal and the user's real decision **before** investing heavily in presentation and UI. Do not assume this exact scientific failure mode applies to every product.
