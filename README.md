# Results Verification & Release Platform

This repository contains the technical artifacts for the **Results Verification & Release Platform** designed for the National Secondary Certificate Council.

The platform supports secure result verification and controlled result release across three main consumer groups:

* Candidates using USSD on feature phones
* Schools downloading results in bulk
* Employers verifying certificates through an API

## Repository Structure
takarda-repo/
│
├── README.md
│
├── api/
│   └── openapi.yaml
│
└── diagrams/
    ├── b1-system-context.mmd
    ├── b2-containers.mmd
    ├── b3-component-verification-service.mmd
    ├── c1-ussd-result-check-sequence.mmd
    ├── c2-school-bulk-download-sequence.mmd
    ├── c3-employer-verification-sequence.mmd
    ├── c4-pin-purchase-sequence.mmd
    └── d1-data-model-er.mmd

## Contents
### API Specification

`api/openapi.yaml` contains the OpenAPI specification for the platform's verification API, including its endpoints, request and response structures, authentication requirements, and documented error responses.

### Architecture Diagrams

The `diagrams/` directory contains the Mermaid source files for the platform's architecture and interaction diagrams.

The diagrams cover:
* System context
* Container architecture
* Verification service components
* USSD result checking
* School bulk downloads
* Employer verification
* PIN purchasing
* Data model

The `.mmd` files contain the Mermaid source so that the diagrams can be reviewed, edited, and rendered independently.

## Validation
The API specification can be linted with Redocly:

```bash
npx @redocly/cli lint api/openapi.yaml

Mermaid diagrams can be previewed in VS Code using the **Markdown Preview Mermaid Support** extension.

## Purpose
These artifacts provide the technical contract and architecture supporting the Results Verification & Release Platform. They are intended to be reviewed alongside the project's requirements and design documents.