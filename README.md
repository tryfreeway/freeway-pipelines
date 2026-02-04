# Freeway Pipelines

Freeway is an on-device speech-to-text app for macOS.
Pipelines let you trigger shell commands with your voice.
Just say a phrase and watch Freeway run the command for you.

This repository contains community pipelines that extend Freeway with quick automations, system shortcuts, and handy utilities.

## Getting Started

Visit https://docs.tryfreeway.com to get started with the Freeway API.
If you want to discover, install, or manage pipelines locally, check out the pipelines section in the documentation for instructions specific to your version of Freeway.

Be sure to read and follow our Pipeline Guidelines before submitting a new pipeline or interacting with others in this repository.

## What You Can Build

Freeway pipelines are simple shell commands triggered by voice patterns.
They can, for example:

- Open URLs or search the web (e.g., "Find in Google…").
- Insert dynamic text like the current date or time.
- Toggle system settings (e.g., show/hide hidden files in Finder).
- Transform selected text (uppercase, lowercase, etc.).
- Create files or run any shell script you can imagine.

Each pipeline lives in its own folder with a trigger pattern and a shell command — that's it.

## Repository Structure

This repository is organized around individual pipelines:
- `pipelines/` – root folder containing all public pipelines.
- `pipelines/<pipeline-name>/` – one pipeline per folder, with its own metadata and command.
  - `meta.json` – describes the pipeline (name, description, author, categories, trigger).
  - `pipeline.json` – contains the actual shell command and match settings.
- `INDEX.json` – contains all pipelines that are available in the Pipelines Library inside the app.

Check existing pipelines to understand the recommended structure, style, and patterns.

## Pipeline Guidelines

To keep the ecosystem healthy and predictable, please follow these rules when publishing a pipeline here:

- Keep the scope focused and understandable at a glance.
- Write shell commands that are safe and predictable — avoid destructive operations without confirmation.
- Avoid hard-coding user-specific paths, secrets, or credentials.
- Be explicit about what your pipeline does, especially if it modifies files or system settings.
- Respect privacy: don't log or transmit user content unless clearly documented and necessary.
- Include a clear license for your pipeline (MIT by default if not specified otherwise).

We may ask you to adjust your pipeline if it conflicts with these guidelines.

## Contributing

We welcome contributions in the form of new pipelines, improvements to existing ones, and documentation updates.

To submit a pipeline:

1. Fork this repository.
2. Create a new branch for your work:
   ```bash
   git checkout -b my-awesome-pipeline
   ```
3. Right-click your pipeline in Freeway, select `Copy Pipeline`, and paste the contents into `pipeline.json`.
4. Add your pipeline under `pipelines/<pipeline-name>/` following the structure and guidelines above.
5. Make sure your pipeline loads and runs correctly in Freeway.
6. Open a pull request against the `main` branch with:
   - A concise title (e.g. `Add open-spotify pipeline`).
   - A brief description of what the pipeline does and how to use it.
   - Links or screenshots/GIFs are welcome but optional.

We review pull requests for functionality, safety, code quality, and documentation clarity.
If a pipeline is experimental, incomplete, or unclear, we may request changes or decide not to merge it.

## Feedback

Freeway pipelines are most useful when shaped by real workflows and feedback.
If you have ideas on how to improve the pipeline system or developer experience, please open an issue in this repository or [contact us](https://tryfreeway.com/contact).
