# Automated Data Ingestion & Discrepancy Management System

> Public case study version of an enterprise project.
> Organization names, data sources, database structures, student information, and confidential business information have been anonymized.

## Overview

This project focuses on automating the ingestion of structured data from multiple external spreadsheet templates into a centralized enterprise database.

The solution standardizes incoming data, validates file structures and business rules, detects discrepancies, and provides operational users with workflows for reviewing and resolving data errors.

## My Role

**Business Analyst**
**Duration:** April 2026 – May 2026

My responsibilities included:

* Requirement elicitation and data-source analysis
* Source-to-target data mapping
* Business rule and validation definition
* Exception and discrepancy workflow design
* SRS documentation
* Logical pseudocode documentation
* Database mapping specification
* UI/UX prototyping
* Collaboration with Developers, QA, Testers, and Technical Leads

## Business Problem

The organization received data from multiple external partners using different spreadsheet structures.

Although the templates contained similar business information, they differed in:

* Column names
* Column positions
* Data formats
* Required and optional fields
* Code systems
* Date formats
* Data types
* Business validation rules

Manual data processing created several risks:

* Incorrect data mapping
* Missing required information
* Duplicate records
* Invalid data formats
* Inconsistent database values
* Long processing times
* Limited visibility into import errors
* Difficulty tracing the original source of discrepancies

## Proposed Solution

```text
External Data Templates
          ↓
File Structure Validation
          ↓
Source-to-Target Mapping
          ↓
Data Transformation
          ↓
Business Rule Validation
          ↓
Discrepancy Classification
          ↓
Manual Review / Correction
          ↓
Centralized Database Ingestion
```

## Key Features

* Multi-template data ingestion
* File structure validation
* Source-to-target data mapping
* Data type validation
* Required field validation
* Duplicate data detection
* Business rule validation
* Automated discrepancy classification
* Manual discrepancy resolution
* Import status tracking
* Data processing history
* Audit logs
* Error report export

## Data Mapping

The system standardizes data from multiple external spreadsheet templates into one centralized database structure.

A source-to-target mapping specification defines:

* Source template
* Source column
* Target database field
* Data type
* Required status
* Transformation rule
* Validation rule
* Default value
* Error handling rule

Example:

| Source Field   | Target Field  | Data Type | Transformation                  |
| -------------- | ------------- | --------: | ------------------------------- |
| Candidate Code | candidate_id  |    String | Trim whitespace                 |
| Full Name      | full_name     |    String | Normalize spacing               |
| Date of Birth  | date_of_birth |      Date | Convert to standard date format |
| Exam Score     | score         |   Decimal | Convert numeric format          |

## Discrepancy Categories

The solution detects and classifies multiple types of discrepancies.

### 1. Missing Required Fields

The imported file does not contain a required column or a required data value is empty.

### 2. Invalid Data Format

A value does not match the expected format, such as:

* Invalid dates
* Non-numeric score values
* Invalid identification codes
* Incorrect email formats

### 3. Duplicate Records

The imported data contains duplicate records based on one or more unique business identifiers.

### 4. Reference Data Mismatch

The imported value does not exist in the corresponding reference data or master data table.

### 5. Business Rule Violation

The imported data passes structural validation but violates a business rule.

Examples include:

* Scores outside the permitted range
* Invalid status combinations
* Inconsistent exam and candidate information
* Records assigned to an incorrect processing period

## Discrepancy Handling Workflow

```text
Discrepancy Detected
        ↓
Discrepancy Classified
        ↓
Record Marked as Invalid
        ↓
Operational User Reviews Error
        ↓
Correct Data / Reject Record
        ↓
System Revalidates Record
        ↓
Valid Data Is Imported
```

## Key Business Rules

### File Structure Validation

Before processing data, the system validates:

* File extension
* Sheet name
* Required columns
* Duplicate column names
* Unexpected columns
* Header row position
* Maximum number of records
* Empty file conditions

### Data Type Validation

The system verifies that each value matches the expected data type:

* Text
* Integer
* Decimal
* Date
* Boolean
* Coded reference value

### Duplicate Detection

Records are checked using one or more unique business keys.

The system distinguishes between:

* Duplicate records within the uploaded file
* Records already existing in the centralized database
* Records previously imported from another source

### Error Processing

Invalid records are not inserted into the production database.

The system:

* Stores the original source value
* Records the validation error
* Identifies the affected field
* Assigns an error category
* Provides a recommended correction
* Allows users to review and correct eligible discrepancies

## AI-Assisted Prototyping

Agentic AI workflows were used to support the generation and iteration of UI prototypes.

The workflow helped:

* Generate initial UI structures
* Convert requirements into screen specifications
* Review UI consistency
* Identify missing states and validation messages
* Accelerate prototype iteration

A total of 32 UI screens were designed and iterated as part of the project.

AI-generated results were reviewed and adjusted based on business requirements, user workflows, and system constraints.

## Deliverables

* Public SRS
* Source-to-Target Data Mapping
* Data Validation Rules
* Business Rules
* Logical Pseudocode
* Discrepancy Classification
* End-to-End Process Diagram
* UI/UX Prototype
* UAT Test Scenarios

## Tools

* Figma
* Draw.io
* SQL
* Microsoft Excel
* Jira
* Confluence
* Agentic AI tools
* UML
* Database Mapping

## Confidentiality Notice

This repository is a public portfolio case study. Organization names, partner names, file templates, database structures, identifiers, personal data, and confidential business rules have been changed or removed.
