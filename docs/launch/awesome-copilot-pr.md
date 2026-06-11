# awesome-copilot External Plugin Submission

## Submission Type

External plugin issue submission for `github/awesome-copilot`.

Current issue:

- `github/awesome-copilot#1973`

## Repository

`https://github.com/televgtamfe-coder/topdown-tutor`

## Plugin Path

`plugins/topdown-tutor`

## Ref And SHA

- Ref: `v0.1.3`
- SHA: `9eb33fcf2f9883636d949c4b251fdf9d3b087947`

## Short Description

A top-down learning skill that explains hard topics clearly, gathers source material, supports canonical-text decomposition, and checks understanding.

## Why It Fits

- It is a reusable skill package rather than a one-off prompt
- It has a clear teaching protocol
- It supports technical, conceptual, and canonical-text topics
- It ships with bilingual README files and example topics

## Submission Notes

- Submitted through the current external plugin issue workflow instead of a direct PR to `plugins/external.json`
- Uses an immutable tag and full commit SHA for review
- Plugin metadata was aligned to `0.1.3` and `shaoshengyi` before submission

## Install Note

```bash
gh skill install televgtamfe-coder/topdown-tutor knowledge-coach --agent codex --scope user --pin v0.1.3
```
