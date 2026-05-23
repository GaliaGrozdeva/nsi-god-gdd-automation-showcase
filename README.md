# NSI / GOD / GDD Automation Showcase

This repository presents the concept and workflow of a desktop tool for preparing Bulgarian annual reporting, corporate tax declaration import data and annual closing control checks.

> This is a public showcase repository.  
> It does not contain production code, client data, accounting databases, real exports, tax declarations or internal mapping logic.

## Purpose

Annual reporting and closing procedures require accountants to collect, review, reconcile and prepare data from multiple accounting sources.

This tool is designed to support Bulgarian annual reporting workflows by preparing data for the annual statistical report, supporting corporate tax declaration import and producing annual closing control checks.

The tool helps prepare:

- data for completing the annual activity report submitted to the National Statistical Institute;
- mandatory internal control checks before final reporting;
- XML output for import of the annual corporate tax declaration based on the official NRA XSD schema;
- annual closing control reports;
- balance and income statement review data;
- source-account explanations showing which accounts from the trial balance and/or general ledger form each reported amount.

The goal is to reduce manual calculations, improve traceability and help accountants focus on professional review instead of repetitive data preparation.

## Core idea

The tool reads accounting exports and prepares reviewable outputs for the accountant.

It is not designed to replace the accountant’s judgment.  
It is designed to show where the figures come from, what accounts form the totals, and which items require review or manual confirmation.

## Key workflow areas

### NSI annual report data preparation

The system extracts and organizes accounting data needed for completing the annual statistical report.

It supports accountant review before filing and helps identify missing, unclear or inconsistent source data.

### Corporate tax declaration XML support

The tool can prepare XML output for import into the Bulgarian National Revenue Agency system for the annual corporate tax declaration, based on the applicable XSD schema.

The XML generation is supported by preview and control logic, so the accountant can review the values before using the file.

### Mandatory internal controls

The application includes internal validation and control checks to reduce the risk of mechanical reporting errors.

Control checks are designed to compare source balances, reporting lines and derived values before final use.

### Annual closing control checks

The tool helps accountants review annual closing positions, account balances and control totals before final reporting.

### Source details for reported amounts

For residual, summarized or controlled reporting lines, the system shows where the amount comes from.

The source detail may include:

- accounts and balances from the trial balance;
- related movements from the general ledger;
- debit or credit balance logic;
- analytical breakdowns where available;
- notes when the source detail is too large and must remain in the original accounting export.

This allows the accountant to trace a reported figure back to the accounting source instead of manually searching through trial balances and ledger reports.

### Review-first logic

If data is unclear, missing, too detailed or not safely mapped, it is marked for review instead of being silently adjusted.

## Input sources

The tool is designed to work with accounting system exports such as:

- trial balance;
- analytical trial balance;
- general ledger;
- structured Excel/HTML/JSON outputs;
- accounting control reports;
- client profile data.

The first internal workflows are based on Megasoft accounting exports.

## Output examples

The tool may prepare:

- data for completing the NSI annual statistical report;
- XML file for annual corporate tax declaration import;
- corporate tax declaration preview data;
- annual closing control report;
- account-source detail reports;
- Excel exports for accountant review;
- issue and missing-data reports;
- validation and control summaries.

## Safety principles

- no automatic accounting corrections;
- no hidden balancing adjustments;
- no invented values;
- review-first workflow;
- source-account traceability;
- clear control reports;
- manual confirmation where required;
- accountant remains responsible for final review and filing.

## Business value

The tool helps accounting teams:

- save time during annual closing;
- reduce repetitive manual calculations;
- identify the source of reported totals;
- detect missing or unclear mappings;
- document review decisions;
- improve control over annual reporting data;
- focus on professional review instead of mechanical preparation.

## Current status

Internal working tool under active development and testing.

The public repository presents the workflow and concept only. Production code, real client data, accounting exports and internal mapping logic are private.

## Development approach

The tool is designed from the annual closing process outward:

1. identify the reporting requirement;
2. collect accounting source data;
3. map accounts to reporting lines;
4. show source details and control checks;
5. mark unclear items for review;
6. prepare accountant-friendly outputs.
