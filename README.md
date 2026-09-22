# ESC — Data Analytics

<p align="center">
  <strong>Data-driven education access, learning, and opportunity.</strong><br />
  <sub>Minimal · measurable · hackathon-ready</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Focus-Education%20Analytics-7357D8?style=for-the-badge" alt="Education analytics" />
  <img src="https://img.shields.io/badge/Benchmark-100%20Tasks-1F8A70?style=for-the-badge" alt="100 task benchmark" />
  <img src="https://img.shields.io/badge/Agents-12-F5A524?style=for-the-badge" alt="12 agents" />
</p>

---

# 01 · THE GAP

```mermaid
flowchart LR
    S[Student<br/>scattered notices] --> G{ACCESS GAP}
    T[Teacher<br/>manual tracking] --> G
    G --> SCH[Missed scholarships]
    G --> ATT[Delayed absence follow-up]
    G --> CAR[Limited career awareness]
    G --> COM[Scattered communication]
    SCH --> E[ESC CONNECT]
    ATT --> E
    CAR --> E
    COM --> E
```

| Challenge | Signal | Response |
|---|---|---|
| Scholarships | Missed deadlines | Match + alerts |
| Careers | Low awareness | Jobs + ITI + internships |
| Attendance | Repeated absence | Follow-up signal |
| Communication | Scattered | School groups |
| Connectivity | Limited data | Text-first UX |

---

# 02 · PRODUCT MAP

```mermaid
flowchart TB
    E[ESC CONNECT]
    E --> O[📣 Opportunities]
    E --> S[🎓 Scholarship Finder]
    E --> C[💬 Academic Community]
    E --> A[📈 Attendance Follow-up]
    O --> O1[Scholarships]
    O --> O2[Internships & Jobs]
    O --> O3[ITI & Career Paths]
    S --> S1[Profile Match]
    S --> S2[Deadlines]
    S --> S3[Documents]
    S --> S4[Official Links]
    C --> C1[Guidance Channels]
    C --> C2[Teacher-Student Groups]
    C --> C3[Moderation]
    A --> A1[Attendance]
    A --> A2[Absence Signal]
    A --> A3[Parent Follow-up]
```

### MVP footprint

```mermaid
xychart-beta
    title "ESC Connect — MVP Modules"
    x-axis ["Opportunities", "Scholarships", "Community", "Attendance"]
    y-axis "Modules" 0 --> 1
    bar [1, 1, 1, 1]
```

---

# 03 · CORE JOURNEYS

### Student

```mermaid
flowchart LR
    P[Profile] --> M[Match] --> V[View] --> S[Save] --> R[Reminder] --> A[Apply]
```

### Teacher

```mermaid
flowchart LR
    T[Mark Attendance] --> D{3+ absences?}
    D -->|YES| F[Follow-up]
    D -->|NO| C[Continue]
    F --> P[Parent Contact]
```

### Pooja

```mermaid
sequenceDiagram
    participant P as Pooja
    participant E as ESC Connect
    participant T as Teacher
    P->>E: Profile
    E-->>P: Likely matches
    P->>E: Save scheme
    P->>T: Ask for guidance
    T-->>P: Guidance
    E-->>P: Deadline reminder
    P->>E: Official application
```

---

# 04 · DATA → ACTION

```mermaid
flowchart LR
    I[Student / Teacher Input]
    I --> P[Profile]
    I --> AT[Attendance]
    I --> O[Opportunities]
    P --> M[Matching]
    AT --> S[Signal]
    O --> F[Feed]
    M --> ACT[Action]
    S --> ACT
    F --> ACT
```

| Input | Processing | Output |
|---|---|---|
| Profile | Eligibility signals | Scholarship match |
| Attendance | Consecutive absence rule | Follow-up |
| Opportunity | Tags + filters | Relevant feed |
| Community | Moderation | Guided communication |

---

# 05 · 12 SPECIALIST AGENTS

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

| Function | Agents |
|---|---:|
| Learning | 2 |
| Assessment | 3 |
| Planning | 2 |
| Revision | 2 |
| Research / resources | 2 |
| Problem solving | 1 |
| **Total** | **12** |

```mermaid
xychart-beta
    title "ESC Agent Distribution"
    x-axis ["Learning", "Assessment", "Planning", "Revision", "Research", "Problem"]
    y-axis "Agents" 0 --> 3
    bar [2, 3, 2, 2, 2, 1]
```

---

# 06 · AI CAPABILITY VIEW

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

```mermaid
flowchart LR
    G[GENERAL AI] --> L[Learn]
    G --> R[Research]
    E[ESC] --> L2[Learn]
    E --> P[Plan]
    E --> V[Revise]
    E --> O[Opportunities]
    E --> S[Scholarships]
    E --> C[Community]
    E --> A[Attendance]
```

---

# 07 · 100-TASK BENCHMARK

```mermaid
flowchart TB
    Q[100 TASKS]
    Q --> R[25 Research]
    Q --> L[25 Learning]
    Q --> V[20 Revision]
    Q --> P[15 Problem Solving]
    Q --> W[15 Productivity]
```

```mermaid
pie title "100-Task Mix"
    "Research" : 25
    "Learning" : 25
    "Revision" : 20
    "Problem Solving" : 15
    "Productivity" : 15
```

### Same test

```mermaid
flowchart LR
    Q[Same 100 Tasks] --> E[ESC]
    Q --> C[ChatGPT]
    Q --> G[Gemini]
    Q --> N[Gemini Notebook]
    Q --> P[Perplexity]
    E --> R[Same Rubric]
    C --> R
    G --> R
    N --> R
    P --> R
```

---

# 08 · SCORING MODEL

```mermaid
pie title "Benchmark Score Weight"
    "Accuracy" : 40
    "Completion" : 30
    "Sources" : 20
    "Instructions" : 10
```

| Metric | Weight |
|---|---:|
| Accuracy | **40%** |
| Completion | **30%** |
| Sources | **20%** |
| Instructions | **10%** |
| **TOTAL** | **100%** |

---

# 09 · ANALYTICS PIPELINE

```mermaid
flowchart LR
    D[Raw Task Data] --> A[Accuracy]
    D --> C[Completion]
    D --> S[Source Support]
    D --> L[Latency]
    A --> X[Score]
    C --> X
    S --> X
    X --> O[Overall]
    X --> CAT[Category]
    L --> TIME[Response Time]
    O --> V[Dashboard]
    CAT --> V
    TIME --> V
```

| Chart | Metric |
|---|---|
| Overall | Score / 100 |
| Category | 5 categories |
| Accuracy | % |
| Completion | % |
| Sources | % |
| Latency | Seconds |

---

# 10 · RESULT DASHBOARD

> **DEMO DATA:** The benchmark values below are illustrative presentation data, not measured results.

### Overall score

```mermaid
xychart-beta
    title "Overall Benchmark — Demo Data"
    x-axis ["ESC", "ChatGPT", "Gemini", "Notebook", "Perplexity"]
    y-axis "Score / 100" 0 --> 100
    bar [93.3, 90.3, 88.4, 88.7, 89.5]
```

### Category performance

```mermaid
xychart-beta
    title "Category Performance — Demo Data"
    x-axis ["Research", "Learning", "Revision", "Problems", "Productivity"]
    y-axis "Score / 100" 0 --> 100
    bar [93.0, 90.0, 88.6, 88.4, 87.6]
```

> **Demo values for presentation only. Replace with measured results before claiming benchmark performance.**

| Tool | Overall | Accuracy | Completion | Sources | Latency |
|---|---:|---:|---:|---:|---:|
| **ESC** | Pending | Pending | Pending | Pending | Pending |
| ChatGPT | Pending | Pending | Pending | Pending | Pending |
| Gemini | Pending | Pending | Pending | Pending | Pending |
| Gemini Notebook | Pending | Pending | Pending | Pending | Pending |
| Perplexity | Pending | Pending | Pending | Pending | Pending |

---

# 11 · CATEGORY DATA

> **Benchmark categories remain pending until the same 100 tasks are run on every tool.**

| Tool | Research | Learning | Revision | Problems | Productivity |
|---|---:|---:|---:|---:|---:|
| **ESC** | Pending | Pending | Pending | Pending | Pending |
| ChatGPT | Pending | Pending | Pending | Pending | Pending |
| Gemini | Pending | Pending | Pending | Pending | Pending |
| Notebook | Pending | Pending | Pending | Pending | Pending |
| Perplexity | Pending | Pending | Pending | Pending | Pending |

```mermaid
flowchart TB
    D[Measured Results]
    D --> R[Research]
    D --> L[Learning]
    D --> V[Revision]
    D --> P[Problem Solving]
    D --> W[Productivity]
```

---

# 12 · ACCESS ANALYTICS

| Tool | Free access | Paid access |
|---|:---:|:---:|
| ESC | ✓ | — |
| ChatGPT | ✓ | ✓ |
| Gemini | ✓ | ✓ |
| Gemini Notebook | ✓ | ✓ |
| Perplexity | ✓ | ✓ |

```mermaid
xychart-beta
    title "Access Model"
    x-axis ["ESC", "ChatGPT", "Gemini", "Notebook", "Perplexity"]
    y-axis "Access tiers" 0 --> 2
    bar [1, 2, 2, 2, 2]
```

`1 = free layer · 2 = free + paid layer`

---

# 13 · LOW-DATA DESIGN

```mermaid
flowchart LR
    U[User] --> T[Text-first]
    U --> C[Compressed media]
    U --> S[Shared-device friendly]
    U --> L[Low-bandwidth UX]
```

| Design choice | Purpose |
|---|---|
| Text-first | Lower data use |
| Compressed media | Faster loading |
| Simple language | Accessibility |
| Shared-device support | Wider access |

---

# 14 · TRUST & SAFETY

```mermaid
flowchart TB
    INFO[Opportunity / Scholarship] --> V[Verified / Reviewed]
    V --> L[Official Link]
    L --> U[User Action]
    CHAT[Community] --> M[Moderation]
    M --> C[Communication]
```

| Rule | Purpose |
|---|---|
| Official links | Reduce misinformation |
| Moderated groups | Safer communication |
| Eligibility = likely | No false guarantee |
| Clear deadlines | Timely action |

---

# 15 · HACKATHON STORY

```mermaid
flowchart LR
    P[Pooja] --> PR[Profile]
    PR --> SM[Scholarship Match]
    SM --> DL[Deadline]
    DL --> AP[Apply]

    T[Teacher] --> AT[Attendance]
    AT --> SG[Absence Signal]
    SG --> FU[Follow-up]
```

---

# 16 · FINAL ANALYTICS MODEL

```mermaid
flowchart LR
    USER[Students + Teachers] --> DATA[Data]
    DATA --> ESC[ESC / ESC Connect]
    ESC --> MATCH[Match]
    ESC --> GUIDE[Guide]
    ESC --> SIGNAL[Signal]
    ESC --> COMM[Communicate]
    MATCH --> ACTION[Action]
    GUIDE --> ACTION
    SIGNAL --> ACTION
    COMM --> ACTION
    ACTION --> METRIC[Measure]
    METRIC --> INSIGHT[Insight]
```

---

## STATUS

| Layer | Status |
|---|---|
| Product map | ✓ |
| User journeys | ✓ |
| 12-agent analytics | ✓ |
| Capability matrix | ✓ |
| 100-task benchmark | ✓ |
| Pie charts | ✓ |
| Bar charts | ✓ |
| Flowcharts | ✓ |
| Actual benchmark results | **Pending** |

> **No fabricated benchmark numbers. Replace result placeholders after identical tests.**
