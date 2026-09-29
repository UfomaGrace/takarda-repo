# Results Verification & Release Platform

This repository contains the technical artifacts for the **Results Verification & Release Platform** designed for the National Secondary Certificate Council.

The platform supports secure result verification and controlled result release across three main consumer groups:

- Candidates using USSD on feature phones
- Schools downloading results in bulk
- Employers verifying certificates through an API

## Repository Structure

```text
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
Each Mermaid `.mmd` source file has a corresponding rendered `.svg` diagram in the same directory.

## Contents

### API Specification

`api/openapi.yaml` contains the OpenAPI specification for the platform's verification API, including:

- API endpoints
- Request and response structures
- Authentication requirements
- Error responses
- PIN purchase and result checks
- School bulk-download jobs
- Certificate verification
- Certificate amendments

The specification was validated using Redocly.

### Architecture Diagrams

The `diagrams/` directory contains the Mermaid source files and rendered SVG diagrams for the platform's architecture and interactions.

The diagrams cover:

- **B1 — System Context**
- **B2 — Container Architecture**
- **B3 — Verification Service Components**
- **C1 — USSD Result Check**
- **C2 — School Bulk Download**
- **C3 — Employer Verification**
- **C4 — PIN Purchase**
- **D1 — Data Model**

The `.mmd` files contain the Mermaid source so that the diagrams can be reviewed, edited, and rendered independently. The `.svg` files provide the rendered versions for viewing and documentation.

## Validation

### OpenAPI

The API specification can be validated with Redocly:

```bash
npx @redocly/cli lint api/openapi.yaml