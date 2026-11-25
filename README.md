# Replication Package: LLMs for Requirements Generation and Quality Assessment

Replication package for the paper "How Valuable Are LLMs for Requirements Generation and Quality Assessment?".

The paper is a systematic literature review (SLR) of 30 primary studies published in 2025–2026 and retrieved from IEEE Xplore. It examines how LLM-based requirements generation affects requirement quality characteristics (RQ1.1) and which contributing factors, root causes, limitations, and solutions are reported for these impacts (RQ1.2); the prompting techniques, architectures, workflows, and input artifacts used for generation (RQ2); and how LLMs are used to detect requirements quality issues and assess requirements quality (RQ3). This package contains the study selection data and the extracted and synthesized data, so that every number and claim in the results can be traced back to the study it came from.

## Contents

```
├── Study_Index.xlsx       one row per primary study: Study ID and its reference number in the paper and in every other file
├── Search_Results.xlsx    the 336 records retrieved from IEEE Xplore, with the screening decisions of both selection stages
├── SLR.xlsx               study selection, quality assessment, and general extracted data (3 sheets)
├── RQ1.xlsx               quality characteristics, impacts, factors, and mapping to standards (6 sheets)
├── RQ2.xlsx               requirements generation approaches (2 sheets)
└── RQ3.xlsx               quality issue detection and assessment methods (2 sheets)
```

## Reading order

| Step | Where | What it contains |
|---:|---|---|
| 1 | `Study_Index.xlsx` | The 30 primary studies (S01–S30) and their reference numbers in the paper and in each spreadsheet. Start here to trace any study. |
| 2 | `Search_Results.xlsx` | All 336 retrieved records with their title/abstract screening decision, ICORE2026 rank, and second-stage decision. |
| 3 | `SLR.xlsx` → `Formal Literature` | The 42 candidate studies that remained after title/abstract screening and the ICORE2026 ranking filter, assessed against the inclusion criteria and the four quality assessment questions. |
| 4 | `SLR.xlsx` → `ReqQua-LLM-dataExt` | General extracted data for the 30 primary studies. |
| 5 | `RQ1.xlsx` → `RQ1_Findings` | Every reported impact on a quality characteristic, with its direction, explanation, and proposed solution (raw extraction). |
| 6 | `RQ1.xlsx` → `Unified-Characteristics`, `RQ1 Results Summary` | How the reported characteristics were grouped into 24 unified characteristics, and the study and finding counts per characteristic. |
| 7 | `RQ1.xlsx` → `Mapping-Characteristics`, `Unmapped StandardFramework Char` | Mapping of the unified characteristics to the QUS framework, ISO/IEC/IEEE 29148:2018, and IEEE Std 830-1993, and the reverse mapping. |
| 8 | `RQ2.xlsx`, `RQ3.xlsx` | Extracted data for RQ2 and RQ3. |

## Study selection

- **Search:** IEEE Xplore, June 16, 2026; publications from 2025–2026; 336 records retrieved.
- **Stage 1:** title and abstract screening against the inclusion criteria → 120 studies; venue rank filter applied to conference papers only, excluding those ranked below B in ICORE2026 → 42 candidates.
- **Stage 2:** full-text reading against the inclusion criteria and quality assessment → 30 primary studies.
- **Quality assessment:** four questions, each scored 0 (No), 1 (Partially), or 2 (Yes); studies scoring at least 4 out of 8 were retained.

## Reference numbers

Each spreadsheet numbers the studies in its own `References` sheet, so the same study has different numbers in different files and in the paper. For example, Kassab and AbdElhameed (2025) is `[35]` in the paper, ID `22` in `SLR.xlsx`, `[6]` in `RQ1.xlsx` and `RQ2.xlsx`, and `[3]` in `RQ3.xlsx`. `Study_Index.xlsx` resolves all of these numbers to a single Study ID.

## The data files

### Study_Index.xlsx

| Column | Content |
|---|---|
| Study ID | S01–S30, ordered by reference number in the paper |
| Full Citation | Full reference of the study |
| Ref. No. in Paper | Reference number in the paper |
| BibTeX Key | Citation key in the paper's bibliography |
| ID in SLR.xlsx | ID used in `SLR.xlsx` |
| Ref. No. in RQ1/RQ2/RQ3.xlsx | Reference number in the `References` sheet of each RQ file (— if the study does not contribute to that RQ) |
| RQ1, RQ2, RQ3 | Whether the study contributes to each RQ (21, 25, and 12 studies, respectively) |

### Search_Results.xlsx

One row per record retrieved from IEEE Xplore (336 rows), exported on June 16, 2026, with the IEEE Xplore metadata (title, authors, venue, year, abstract, DOI, keywords, etc.) and the following screening columns.

| Column | Content |
|---|---|
| Source Type | Conference paper, journal article, magazine article, early access article, book chapter, or standard |
| Related Research Question(s) | RQs to which the study contributes (included studies only) |
| ICORE Rank | ICORE2026 rank of the conference (A*, A, B, C), `Not Listed` (conference not in the ranking), `National: Country` (national venue), `Not Applicable` (not a conference paper), or `Not Screened` (excluded at title/abstract screening, so the rank was not checked) |
| In/Out (Title + Abstract + ICORE) | 1 if retained after stage 1 (42 studies), 0 otherwise |
| In/Out (Second Evaluation) | 1 if retained after stage 2 (30 primary studies), 0 otherwise |

Row colors summarize the decisions:

| Color | Meaning | Records |
|---|---|---:|
| Red | Excluded at title/abstract screening | 216 |
| Orange | Passed title/abstract screening, excluded by the venue rank filter | 78 |
| Blue | Excluded at the second stage (full-text reading, inclusion criteria, quality assessment) | 12 |
| Green | Included as primary study | 30 |

### SLR.xlsx

**`Formal Literature`**: one row per candidate study (42 rows).

| Column | Content |
|---|---|
| Source, Paper Name, Full Citation | Identification of the study |
| Inclusion Criteria | Yes/No for each inclusion criterion |
| Inclusion Status | Final inclusion decision |
| Quality Assessment Questions | Score per question: 0 (No), 1 (Partially), 2 (Yes) |
| Quality Score | Sum of the four scores, out of 8 (threshold: 4) |

**`ReqQua-LLM-dataExt`**: one row per primary study (30 rows): ID, full citation, summary, theoretical foundation, methodology, dataset/context, accessibility of materials, findings, strengths and limitations, and short notes per research question.

**`RQs-searchTerms`**: the research questions and the search terms derived from them.

### RQ1.xlsx

**`RQ1_Findings`**: the raw extraction for RQ1, one row per reported finding.

| Column | Content |
|---|---|
| Characteristic | Quality characteristic as named and defined in the study |
| Finding Evidence | Evidence for the finding as reported in the study |
| Direction | Positive (improvement) or Negative (quality problem) |
| Finding (Impact) | Description of the impact |
| Contributing Factor (CF) / Root Cause (RC) / Limitation (L) | Reported explanation of the impact, or "Not Reported" |
| Proposed Solution | Reported or recommended solution |
| Reference | Study, numbered as in the `References` sheet |

**`Unified-Characteristics`**: one row per unified characteristic (24 rows): the original labels and studies grouped under it, and the positive and negative themes with their supporting findings.

**`RQ1 Results Summary`**: one row per unified characteristic: number of primary studies, positive findings, and negative findings.

**`Mapping-Characteristics`**: one row per unified characteristic: its definitions in the studies, the corresponding characteristic in the QUS framework, ISO/IEC/IEEE 29148:2018, and IEEE Std 830-1993 (or "No mapping identified"), and a justification.

**`Unmapped StandardFramework Char`**: characteristics of the standards and framework with no counterpart among the unified characteristics.

### RQ2.xlsx

**`RQ2_Data_Extraction`**: one row per primary study (25 rows).

| Column | Content |
|---|---|
| Requirement Generation Task, Output Artifact | What is generated |
| Prompting Technique / Strategy, Prompting Details | Prompting technique used |
| Architecture, Architecture Details | Architectural approach (e.g., single LLM, multi-LLM, multi-agent, RAG, hybrid) |
| Workflow Strategy, Workflow Details | Workflow (e.g., sequential, iterative refinement, human feedback) |
| Input Artifact / Source, Input Details | Input artifacts used for generation |
| Model(s) | LLMs used |
| Notes / Evidence | Additional evidence |
| Reference | Study, numbered as in the `References` sheet |

### RQ3.xlsx

**`RQ3_Data_Extraction`**: one row per primary study (12 rows).

| Column | Content |
|---|---|
| Quality Characteristics Examined | Quality issues or characteristics addressed |
| LLM's Role in Quality Defect Detection / Assessment | What the LLM does |
| Prompting Techniques | Prompting technique used |
| Detection / Assessment Strategies | How detection or assessment is performed |
| Quality Criteria / Frameworks | Criteria, scales, or frameworks applied |
| Evaluation / Validation Methods | How the LLM's detection or assessment was validated |
| Detection / Assessment Outputs | Output produced by the LLM |
| Notes / Evidence | Additional evidence |
| Reference | Study, numbered as in the `References` sheet |

## Worked example

`RQ1 Results Summary` reports that **Completeness** was examined in 6 studies, with 4 positive and 5 negative findings. Filtering `RQ1_Findings` for the characteristics grouped under Completeness in `Unified-Characteristics` gives these findings and their references. One of them, reference `[6]`, reports a positive finding (multi-LLM ensembles substantially improved recall in detecting missing requirements) and a negative one (individual LLMs achieved low and highly variable recall). Looking up `[6]` in the *Ref. No. in RQ1.xlsx* column of `Study_Index.xlsx` identifies the study as S23, Kassab and AbdElhameed (2025), which is cited as `[35]` in the paper.

## Contact

Çiğdem Coşkuner (cigdem.coskuner@metu.edu.tr)
