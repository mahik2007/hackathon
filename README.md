# ESC — Data Analytics
### Hackathon Analytics Dashboard

---

## 01 · PROBLEM → SOLUTION

```mermaid
flowchart LR
    S[STUDENT] --> G[ACCESS GAP]
    T[TEACHER] --> G
    G --> SCH[Scholarships]
    G --> CAR[Careers]
    G --> ATT[Attendance]
    G --> COM[Communication]
    SCH --> E[ESC CONNECT]
    CAR --> E
    ATT --> E
    COM --> E
```

| Gap | Signal | ESC Connect |
|---|---|---|
| Scholarships | Missed deadline | Match + reminder |
| Careers | Low awareness | Jobs + ITI + internships |
| Attendance | Repeated absence | Follow-up |
| Communication | Scattered | Community |

---

## 02 · PRODUCT ARCHITECTURE

```mermaid
flowchart TB
    E[ESC CONNECT]
    E --> O[OPPORTUNITIES]
    E --> S[SCHOLARSHIP FINDER]
    E --> C[ACADEMIC COMMUNITY]
    E --> A[ATTENDANCE]
    O --> O1[Scholarships]
    O --> O2[Internships]
    O --> O3[Jobs / ITI]
    S --> S1[Profile]
    S --> S2[Eligibility]
    S --> S3[Deadline]
    S --> S4[Documents]
    C --> C1[Teacher]
    C --> C2[Student]
    C --> C3[Guidance]
    A --> A1[Attendance]
    A --> A2[3+ Absence]
    A --> A3[Follow-up]
```

---

## 03 · USER JOURNEY

```mermaid
flowchart LR
    P[Profile] --> M[Match]
    M --> V[View]
    V --> S[Save]
    S --> R[Reminder]
    R --> A[Apply]
```

```mermaid
sequenceDiagram
    participant P as Student
    participant E as ESC Connect
    participant T as Teacher
    P->>E: Profile
    E-->>P: Match
    P->>E: Save
    P->>T: Ask
    T-->>P: Guidance
    T->>E: Attendance
    E-->>T: Follow-up
```

---

## 04 · ATTENDANCE SIGNAL

```mermaid
flowchart LR
    T[Teacher] --> A[Mark Attendance]
    A --> D{3+ absences?}
    D -->|YES| F[Follow-up]
    D -->|NO| C[Continue]
    F --> P[Parent Contact]
```

| Input | Rule | Output |
|---|---|---|
| Attendance | 3+ consecutive | Follow-up |
| Teacher action | Review | Contact |
| Goal | Early signal | Reduce dropout risk |

---

# 05 · ESC CORE — 12 AGENTS

```mermaid
flowchart TB
    E((ESC))
    E --> A1[StudyVault]
    E --> A2[ExamInsight]
    E --> A3[SuccessArchitect]
    E --> A4[Concept Clarifier]
    E --> A5[Problem Solver]
    E --> A6[QuizForge]
    E --> A7[Revision Coach]
    E --> A8[Flashcard Studio]
    E --> A9[MindMap Maker]
    E --> A10[Resource Scout]
    E --> A11[Paper Pattern Analyst]
    E --> A12[GuideMinds]
```

| Agent | Role |
|---|---|
| StudyVault | Sources |
| ExamInsight | Assessment |
| SuccessArchitect | Planning |
| Concept Clarifier | Learning |
| Problem Solver | Problems |
| QuizForge | Practice |
| Revision Coach | Revision |
| Flashcard Studio | Recall |
| MindMap Maker | Synthesis |
| Resource Scout | Resources |
| Paper Pattern Analyst | Exam patterns |
| GuideMinds | Actions |

---

# 06 · CAPABILITY MATRIX

| Capability | ChatGPT | Gemini | Gemini Notebook | Perplexity | **ESC** |
|---|:---:|:---:|:---:|:---:|:---:|
| AI chat | ✓ | ✓ | ✓ | ✓ | ✓ |
| Files | ✓ | ✓ | ✓ | ✓ | ✓ |
| Learning | ✓ | ✓ | ✓ | △ | ✓ |
| Research | ✓ | ✓ | ✓ | ✓ | ✓ |
| Citations | ✓ | ✓ | ✓ | ✓ | ✓ |
| Quiz / practice | ✓ | ✓ | ✓ | △ | ✓ |
| Revision | ✓ | ✓ | ✓ | △ | ✓ |
| Planning | ✓ | ✓ | △ | △ | ✓ |
| Specialist agents | △ | △ | △ | △ | **12** |
| Scholarships | — | — | — | — | **✓** |
| Jobs / ITI | — | — | — | — | **✓** |
| Teacher communication | — | — | — | — | **✓** |
| Attendance follow-up | — | — | — | — | **✓** |
| Low-data focus | — | — | — | — | **✓** |

`✓ documented · △ limited / plan-dependent · — not a core documented focus`

---

# 07 · COVERAGE VIEW

```mermaid
flowchart LR
    G[GENERAL AI]
    G --> L[Learn]
    G --> R[Research]
    E[ESC]
    E --> L2[Learn]
    E --> P[Plan]
    E --> V[Revise]
    E --> O[Opportunities]
    E --> S[Scholarships]
    E --> C[Community]
    E --> A[Attendance]
```

| Layer | ESC |
|---|:---:|
| Learn | ✓ |
| Research | ✓ |
| Plan | ✓ |
| Revise | ✓ |
| Opportunities | ✓ |
| Scholarships | ✓ |
| Community | ✓ |
| Attendance | ✓ |

---

# 08 · 100-TASK BENCHMARK

```mermaid
flowchart TB
    Q[100 TASKS]
    Q --> R[25 Research]
    Q --> L[25 Learning]
    Q --> V[20 Revision]
    Q --> P[15 Problem Solving]
    Q --> W[15 Productivity]
```

### Task mix

```mermaid
pie title 100-Task Mix
    "Research" : 25
    "Learning" : 25
    "Revision" : 20
    "Problem Solving" : 15
    "Productivity" : 15
```

---

# 09 · TEST PIPELINE

```mermaid
flowchart LR
    Q[Same 100 Tasks]
    Q --> E[ESC]
    Q --> C[ChatGPT]
    Q --> G[Gemini]
    Q --> N[Gemini Notebook]
    Q --> P[Perplexity]
    E --> R[Same Rubric]
    C --> R
    G --> R
    N --> R
    P --> R
    R --> D[Measured Data]
```

| Control | Same? |
|---|:---:|
| Prompt | ✓ |
| Source | ✓ |
| Task | ✓ |
| Rubric | ✓ |
| Model tier | ✓ where possible |
| Date | Record |
| Latency | Record |

---

# 10 · SCORING MODEL

| Metric | Weight |
|---|---:|
| Accuracy | **40%** |
| Completion | **30%** |
| Sources | **20%** |
| Instructions | **10%** |
| **TOTAL** | **100%** |

```mermaid
pie title Score Weight
    "Accuracy" : 40
    "Completion" : 30
    "Sources" : 20
    "Instructions" : 10
```

---

# 11 · BENCHMARK DATA TABLE

| Tool | Overall | Accuracy | Completion | Sources | Latency |
|---|---:|---:|---:|---:|---:|
| **ESC** | — | — | — | — | — |
| ChatGPT | — | — | — | — | — |
| Gemini | — | — | — | — | — |
| Gemini Notebook | — | — | — | — | — |
| Perplexity | — | — | — | — | — |

> `— = test pending`

---

# 12 · CATEGORY DATA

| Tool | Research | Learning | Revision | Problems | Productivity |
|---|---:|---:|---:|---:|---:|
| ESC | — | — | — | — | — |
| ChatGPT | — | — | — | — | — |
| Gemini | — | — | — | — | — |
| Notebook | — | — | — | — | — |
| Perplexity | — | — | — | — | — |

```mermaid
flowchart TB
    D[Task Results]
    D --> R[Research]
    D --> L[Learning]
    D --> V[Revision]
    D --> P[Problems]
    D --> W[Productivity]
```

---

# 13 · ANALYTICS DASHBOARD

```mermaid
flowchart TB
    D[RAW RESULTS]
    D --> S[Overall Score]
    D --> A[Accuracy]
    D --> C[Completion]
    D --> R[Source Support]
    D --> L[Latency]
    S --> G1[Overall Chart]
    A --> G2[Accuracy Chart]
    C --> G3[Completion Chart]
    R --> G4[Source Chart]
    L --> G5[Latency Chart]
```

### Chart set

| Chart | Data |
|---|---|
| Overall | Score / 100 |
| Category | 5 task groups |
| Accuracy | % |
| Completion | % |
| Sources | % |
| Latency | Seconds |

---

# 14 · CHART-READY RESULT GRID

| Tool | Score | Accuracy | Completion | Sources | Latency |
|---|---:|---:|---:|---:|---:|
| ESC | TBD | TBD | TBD | TBD | TBD |
| ChatGPT | TBD | TBD | TBD | TBD | TBD |
| Gemini | TBD | TBD | TBD | TBD | TBD |
| Notebook | TBD | TBD | TBD | TBD | TBD |
| Perplexity | TBD | TBD | TBD | TBD | TBD |

```mermaid
flowchart LR
    T[TEST] --> C[COLLECT]
    C --> S[SCORE]
    S --> V[VISUALIZE]
    V --> I[INSIGHT]
```

---

# 15 · ACCESS

| Tool | Free | Paid |
|---|:---:|:---:|
| ESC | ✓ | — |
| ChatGPT | ✓ | ✓ |
| Gemini | ✓ | ✓ |
| Gemini Notebook | ✓ | ✓ |
| Perplexity | ✓ | ✓ |

```mermaid
flowchart LR
    F[FREE ACCESS]
    F --> E[ESC]
    F --> C[ChatGPT]
    F --> G[Gemini]
    F --> N[Notebook]
    F --> P[Perplexity]
```

---

# 16 · DATA SOURCES

| Source | Used for |
|---|---|
| OpenAI Study Mode | Learning / files / practice |
| OpenAI Deep Research | Research |
| Google Gemini Help | Research / files |
| Google | Gemini Notebook |
| Perplexity Help | Search / citations / files |
| Google One | Plan / access |
| Anthropic | Claude ecosystem |

---

# 17 · HACKATHON STORY

```mermaid
flowchart LR
    P[Pooja] --> S[Profile]
    S --> M[Scholarship Match]
    M --> D[Deadline]
    D --> A[Application]

    T[Teacher] --> AT[Attendance]
    AT --> X[3+ Absence]
    X --> F[Follow-up]
```

---

# 18 · FINAL DATA FLOW

```mermaid
flowchart LR
    USERS[Students + Teachers]
    USERS --> INPUT[Data]
    INPUT --> ESC[ESC / ESC Connect]
    ESC --> MATCH[Match]
    ESC --> GUIDE[Guide]
    ESC --> SIGNAL[Signal]
    ESC --> COMM[Communicate]
    MATCH --> OUT[Action]
    GUIDE --> OUT
    SIGNAL --> OUT
    COMM --> OUT
```

## STATUS

| Layer | Status |
|---|---|
| Product analytics | ✓ |
| Capability data | ✓ |
| Benchmark design | ✓ |
| Benchmark results | **Pending** |
| Result charts | **Fill after testing** |

**Rule:** no fabricated benchmark numbers.
