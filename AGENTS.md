# AGENTS.md

## Project purpose

This repository manages Bukky's AI illustration production workflow, including workflow definitions, step requirements, layout templates, prompt templates, evaluation rules, and Drive operation rules.

## Always refer to these documents

- `workflow/`
- `step_requirements/`
- `db/`
- `templates/`
- `rules/`

## Core operating rules

- Follow the main workflow definition unless the user explicitly requests an extra workflow.
- Stop after each Step and wait for the user's "次へ" instruction before continuing.
- Extra workflows are executed only when requested in the initial instruction or explicitly connected after the final Step.
- Always check the image evaluation knowledge base before creating prompts, evaluating generated images, or proposing fixes.
- After generating or receiving an image, create an evaluation summary and identify any issues.
- If a new recurring issue is found, propose an update to the image evaluation knowledge base.
- Use Google Drive as the output workspace for generated images, evaluation documents, handoff notes, and management spreadsheets.
- Do not overwrite existing files unless the user explicitly instructs it.
- Prefer versioned filenames such as `_v1_0`, `_v1_1`, `_updated`, or date-based names.
- Treat GitHub as the source of truth for workflow rules, templates, and automation scripts.
- Treat Google Drive as the storage area for generated assets, evaluation documents, and production logs.
