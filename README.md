# TopDown Tutor

[中文说明](./README.zh-CN.md)

Teach hard topics from the top down, gather the right materials, and check whether the learner actually understood them.

TopDown Tutor starts with plain-language understanding, then goes deeper in layers. It keeps source quality high, supports overview + original text + decomposition, and adds focused understanding checks instead of dumping information.

## What It Is

TopDown Tutor is a reusable learning skill package built for agent-driven teaching.

It helps with four jobs in one flow:

1. Turn a topic into a teachable map.
2. Gather the right materials instead of making the learner search first.
3. Explain the topic from simple to deep.
4. Check understanding with a small number of high-value questions.

It is designed for topics that are easy to make confusing:

- technical topics such as APIs or React Hooks
- concept-heavy topics such as probability
- canonical-text topics such as *The Art of War*
- theory-heavy topics that need both overview and source contact

## Why It Is Different

Most learning prompts stop at "explain this." TopDown Tutor is stricter.

- It teaches in a fixed order: overall picture, distinctive features, internal logic, top 10 knowledge points.
- It starts with plain-language understanding, but it does not downgrade source authority just because the explanation is easier.
- It supports overview + original text + decomposition for canonical-text topics.
- It asks up to three key checks instead of scattering many questions.
- It gives one simple example for each new knowledge point.
- It translates technical terms or English terms on first mention with the original term, Chinese translation, and a plain Chinese explanation.

## How It Teaches

The teaching rhythm is fixed:

1. Zero-start overview when needed
2. Overall picture
3. Distinctive features
4. Internal logic
5. Top 10 knowledge points
6. Key checks

Each topic is explained in three layers:

1. Plain-language understanding
2. Accurate everyday explanation
3. More technical explanation

Every new knowledge point gets:

- one simple example
- one clearer term explanation if technical or English wording appears
- one role or environment application when the learner context is known

## How It Gets Materials

TopDown Tutor does not treat all topics the same.

- Library, framework, API, or tool topics prefer official docs, official examples, and primary references.
- Broad concept topics prefer textbooks, review material, and reputable educational sources.
- Historical, political, intellectual, or canonical-text topics prefer overview sources plus direct source material plus decomposition notes.
- Applied topics prefer worked examples and practice tasks.

The core rule is simple:

**Make the explanation easier. Do not lower the authority level of the source unless the learner explicitly asks for that.**

## Original Texts and Decomposition

When a topic has important original texts, TopDown Tutor keeps both routes:

1. Overview
2. Original text
3. Decomposition

That means the learner gets orientation first, then contact with the source material, then a breakdown of:

- historical context
- core claim
- plain-language meaning
- important terms
- why the text matters
- common misunderstandings

This avoids two common failures:

- staying forever at summary level
- throwing raw original text at the learner without support

## Install

GitHub CLI `gh 2.90.0+` is recommended for public installation.

Install for Codex at user scope:

```bash
gh skill install televgtamfe-coder/topdown-tutor knowledge-coach --agent codex --scope user
```

Preview before install:

```bash
gh skill preview televgtamfe-coder/topdown-tutor knowledge-coach
```

Install from a local checkout:

```bash
gh skill install D:\topdown-tutor knowledge-coach --from-local --dir C:\Users\MeetYou\.codex\skills --force
```

## Usage

Example prompts:

```text
Teach me what an API is from the top down. Gather the right materials and check whether I really understood it.
```

```text
Teach me React Hooks from the top down. Keep it easy to understand, but do not downgrade the source level.
```

```text
Teach me probability from the top down with examples and key checks.
```

```text
Teach me The Art of War as a canonical-text topic using overview + original text + decomposition.
```

## Example Topics

See the ready-made examples in [`examples/`](./examples):

- [`api.md`](./examples/api.md)
- [`react-hooks.md`](./examples/react-hooks.md)
- [`probability.md`](./examples/probability.md)
- [`the-art-of-war.md`](./examples/the-art-of-war.md)

## Output Format

The expected output shape is:

1. One-sentence topic definition
2. Overall map
3. Distinctive features
4. Internal logic
5. Top 10 knowledge points
6. One simple example per new point
7. Term translation support on first mention
8. Up to three key checks

For canonical-text topics it also includes:

1. Overview sources
2. Original text picks
3. Decomposition path

## Repository Structure

```text
topdown-tutor/
|- assets/
|- docs/
|  `- launch/
|- examples/
`- skills/
   `- knowledge-coach/
      |- SKILL.md
      |- agents/
      `- references/
```

## Roadmap

- Stabilize the public skill package
- Publish the first GitHub release
- Add the optional Codex plugin wrapper
- Expand example coverage
- Add release notes and contribution workflows

## FAQ

### Does "plain-language" mean child-level material?

No. It means easier explanation, not lower-authority material.

### Does this only work for technical topics?

No. It also works for concept-heavy and canonical-text topics.

### Does it always ask many questions?

No. It keeps each round focused to up to three key checks.

### Does it support original texts?

Yes. That is one of the core design choices.

## Contributing

Issues, examples, README improvements, and packaging fixes are all welcome.

When contributing, keep the core rules stable:

- plain-language explanation first
- no silent source downgrade
- overview + original text + decomposition for canonical-text topics
- up to three key checks per round

## License

No open-source license has been selected yet. Add one before broad external redistribution if you want clear reuse rights.
