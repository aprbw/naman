---
name: naman
description: NAMAN (Arian's Moniker And Nomenclature) executes a 6-phase cognitive funnel to generate robust, constraint-optimized skill identifiers based on Arian's Master Desiderata.
author_website: https://www.arianprabowo.com
---

# NAMAN: Arian's Moniker And Nomenclature

Use this skill to generate high-fidelity names/identifiers for AI skills and tools based on specific design principles.

**Input Handling:** The user's input could be anything—a short phrase or a long document. If the user provides input, you must extract seeds and generate candidates (do not refuse vague input). **However, if the user invokes the skill with absolutely no input or context whatsoever, you must STOP and ask for clarification rather than guessing their intent.**
**Multiplication Factor (M):** The user may optionally specify a multiplication factor `M` (between 2 and 10, default is 3). If the user requests an `M` > 10, strictly cap it at 10. This factor controls the volume of generation across the funnel.

## ARIAN'S MASTER DESIDERATA
Please refer to `references/desiderata.md` for the strict hard gates and soft gate saturation scoring system you MUST apply during generation.

## Execution Pipeline (6-Phase Funnel)

**FORMAT NOTE:** Please refer to `references/audit_trail_schema.md` for the strict fixed format you MUST use for the `audit_trail.md` artifact across all phases.

### 1. Semantic Seed Extraction
Extract `M` semantic keywords (state changes, topologies, functions) from the input. Write seeds to the `audit_trail.md` artifact.

### 2. Divergent Semantic Radiation
Generate `M` divergent synonyms/metaphors per seed (`M^2` total). Append to `audit_trail.md`.

### 3. Generation Matrix (Scale-Out Expansion)
Translate the `M^2` concepts into target lexicons, generating `M` variations per concept (`M^3` total strings). Apply palindrome/recursive engineering.
**CRITICAL:** To avoid token limits, you must default to **Parallel Subagent Delegation (Map-Reduce)** if your environment allows it. Spawn multiple background subagents and assign each a slice of the concepts to process concurrently. If subagents are NOT supported by your environment, fallback to multi-turn iterative execution: generate 50-100 candidates per turn, appending to `audit_trail.md` before taking the next turn, looping until all `M^3` are saved.

### 4. Algorithmic Grading & Pruning (Scale-Out Execution)
Apply **Hard Gates** to cull, and **Soft Gates** to score the `M^3` candidates.
**CRITICAL:** As with Phase 3, default to **Parallel Subagent Delegation** to score candidates concurrently if supported. If subagents are not supported, fallback to multi-turn execution: process in batches of 50-100 per turn and append results to `audit_trail.md` iteratively. Finally, sort the global survivors by cumulative score.

### 5. Taxonomic Clustering
Select the top 10-20 highest-scoring candidates. Enforce taxonomic isolation by clustering the finalists into 3-5 distinct groups based on their typology and archetype (e.g., The Nusantara Cluster, The Manga Lore Cluster, The Palindrome Cluster, The Recursive Acronym Cluster).

### 6. Payload Delivery
Deliver the final payload directly into the chat in the exact format specified below. Additionally, create a Markdown Artifact (e.g., `audit_trail.md`) that serves as a comprehensive audit trail containing everything at every step of the funnel (all extracted seeds, the full list of ~100 radiated concepts, the massive ~1,000 candidate generation matrix, and the detailed grading/pruning results).

## Output Schema
Please refer to `references/output_schema.md` for the exact output format (Cognitive Scratchpad and Taxonomic Clusters) you MUST use to deliver the payload.