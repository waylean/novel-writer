<p align="center">
  <img src="assets/novel-writer-wordmark.svg" alt="Novel Writer wordmark" width="820">
</p>

<p align="center">
  <a href="README.zh-CN.md">中文</a> · <a href="README.md">English</a>
</p>

A reusable `SKILL.md` workflow for writing long-form novels with AI agents.

Instead of asking an AI to remember an entire book in one chat, this skill turns a novel into a durable project: canon files, chapter contracts, drafts, reviews, research notes, and memory ledgers.

## Why This Exists

AI can write fluent scenes, but long novels fail when the model forgets character state, changes the main plot, reveals secrets too early, or lets characters act out of convenience.

This skill solves that by making the agent behave like a disciplined writing room assistant:

- build the story bible before drafting
- write from approved chapter contracts
- review every chapter for continuity
- track character state and plot threads outside the chat window
- learn from the author's edits so future drafts need less manual repair

## Who This Is For

- web-novel writers
- serial fiction authors
- game writers
- screenwriters prototyping long arcs
- prompt engineers building fiction workflows
- anyone who wants AI help but still wants control over canon

## What It Does

- Initializes a complete novel project folder.
- Creates and maintains `canon/`, `outline/`, `memory/`, `drafts/`, `reviews/`, and `research/`.
- Forces each chapter through a contract before prose drafting.
- Checks chapter drafts against approved canon.
- Tracks who knows what, which secrets remain hidden, and which plot threads are unpaid.
- Converts the author's revisions into an `author_editing_profile`.
- Supports trend and hook research without pasting raw memes into prose.

## Installation

Copy the `novel-writer/` folder into your agent's skills directory.

For Codex:

```text
C:\Users\<you>\.codex\skills\novel-writer
```

For Claude Code:

```text
~/.claude/skills/novel-writer
```

Restart the agent if it does not detect the skill.

If your tool does not support automatic skill loading, open `novel-writer/SKILL.md`, copy the core rules into your system prompt or project instructions, and use `references/` as project knowledge.

## Usage

Then open or create a novel folder and say:

```text
Use the novel-writer skill.
Initialize this folder as a long-form novel project.
Do not write prose yet.
First help me turn my theme, core ideas, target readers, taboo content, and ending direction into proposals.
```

## Model Compatibility

This skill works best with AI agents that can read and write local files and follow multi-step instructions. It is not tied to one model provider.

Recommended:

- Codex with a strong reasoning/coding model.
- Claude Code with Skills support.
- Any agent that supports `SKILL.md`, local file tools, and long project workflows.

## Basic Workflow

1. Author gives theme, core idea, target readers, style references, taboo content, and ending preference.
2. Agent creates proposals, not canon.
3. Author approves the direction.
4. Agent writes approved material into `canon/` and `outline/`.
5. Agent prepares a chapter contract.
6. Author approves the chapter contract.
7. Agent drafts the chapter.
8. Agent writes a continuity review.
9. Author revises.
10. Agent learns from the revision and updates the editing profile.

## Case Study

The `examples/假如我成为了反派/` folder shows how the workflow applies to a working Chinese web-novel project.

The `chapters/` folder includes the first 11 chapters so users can judge the prose quality directly. The analysis file explains how the workflow improves causality, hooks, protagonist agency, antagonist competence, rule placement, and moral cost.

## License

MIT License.
