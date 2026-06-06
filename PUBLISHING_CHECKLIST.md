# Publishing Checklist

## Recommended Positioning

Publish as a **skill-first** project:

```text
ai-novel-writer-skill/
  README.md
  README.zh-CN.md
  PUBLISHING_CHECKLIST.md
  CHANGELOG.md
  LICENSE
  novel-writer/
  examples/
```

Add a harness later if you want automated tests, sample project generation, chapter-review benchmarks, or model comparisons.

## README Should Include

- One-sentence project promise.
- What problem it solves.
- Installation instructions.
- First-use prompt.
- Example workflow.
- Case study summary.
- License.
- Model compatibility.
- Simple installation instructions.
- What example chapter text is included.

## Skill Folder Should Include

- `SKILL.md`: concise core workflow and trigger description.
- `references/`: schemas, chapter workflow, human edit loop.
- `scripts/init_novel_project.py`: deterministic project setup.
- `agents/openai.yaml`: UI metadata when supported.

## License

Current license: MIT, copyright holder `waylean`.

## Before Publishing

- Decide whether to include English, Chinese, or both README files.
- Confirm that publishing the first 11 example chapters is intended.
- Run the skill validator if available.
- Test `scripts/init_novel_project.py` in a blank folder.
- Do not publish low-quality poster drafts or local experiment assets.
