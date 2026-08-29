# Audit Trail Schema

The `audit_trail.md` artifact MUST strictly follow this format for all phases to ensure reproducibility and transparency.

## Phase 1: Semantic Seeds
- **[Seed 1]**:
  - **Description**: [Brief description of what this seed represents]
  - **Quote**: "[Verbatim quote from the input]"
  - **Core**: [Why this seed is core to the context]
- **[Seed 2]**:
  - **Description**: [Brief description]
  - **Quote**: "[Verbatim quote]"
  - **Core**: [Why it is core]
*(M seeds total)*

## Phase 2: Divergent Radiation
For each Phase 1 seed, organize the M radiated concepts by their semantic vector.
- **[Seed 1]**:
  - **[Vector 1]**: [Concept 1], [Concept 2]
  - **[Vector 2]**: [Concept 3]
*(M concepts per seed, M^2 concepts total)*

## Phase 3: Generation Matrix
A strict 3-level nested bullet list containing exactly `M^3` entries.
- **[Seed 1]**:
  - **[Concept 1]**:
    - [Candidate 1] - [Expansion/Recursive Acronym if applicable]
    - [Candidate 2]
*(M^3 variations total)*

## Phase 4: Algorithmic Grading & Pruning
A markdown table containing exactly `M^3` rows, explicitly evaluating every single candidate. NO PRUNING OR OMITTING FOR BREVITY IS ALLOWED.

| #   | Source (Phase 1 -> Phase 2) | Candidate   | Expansion   | Hard Gates         | Soft Gates Passed      | Soft Gates Score |
| -----| -----------------------------| -------------| -------------| --------------------| ------------------------| ------------------|
| 1   | [Seed] -> [Concept]         | [Candidate] | [Expansion] | [Pass/Fail reason] | [List of passed gates] | [Score]          |
*(M^3 rows total)*
