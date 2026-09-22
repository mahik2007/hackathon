# ESC — Data Analytics

## 1. GAP

```mermaid
flowchart LR
    S[Students] --> G[Access Gap]
    T[Teachers] --> G
    G --> A[Scholarships]
    G --> B[Career Access]
    G --> C[Attendance]
    G --> D[Communication]
    A --> E[ESC Connect]
    B --> E
    C --> E
    D --> E
```

```mermaid
flowchart TB
    P[Pooja] --> S[Scattered information]
    S --> M[Missed opportunity]
    M --> E[ESC Connect]
    E --> F[Match]
    F --> R[Reminder]
    R --> L[Official Link]
```

| Gap | ESC Connect |
|---|---|
| Scholarships | Match + deadline |
| Careers | Jobs + ITI + internships |
| Attendance | Absence signal |
| Communication | Groups + guidance |

---

## 2. PRODUCT MAP

```mermaid
flowchart TB
    E[ESC Connect]
    E --> O[Opportunities]
    E --> S[Scholarships]
    E --> C[Community]
    E --> A[Attendance]
    O --> O1[Jobs]
    O --> O2[Internships]
    O --> O3[ITI]
    S --> S1[Profile]
    S --> S2[Documents]
    S --> S3[Deadline]
    C --> C1[Teacher]
    C --> C2[Student]
    A --> A1[Absence]
    A --> A2[Follow-up]
```

---

## 3. USER FLOW

```mermaid
flowchart LR
    U[Student] --> P[Profile]
    P --> M[Match]
    M --> V[View]
    V --> S[Save]
    S --> R[Reminder]
    R --> A[Apply]
```

```mermaid
sequenceDiagram
    participant S as Student
    participant E as ESC Connect
    participant T as Teacher
    S->>E: Profile
    E-->>S: Matches
    S->>E: Save
    S->>T: Ask
    T-->>S: Guidance
    T->>E: Attendance
    E-->>T: Follow-up
```

---

## 4. ATTENDANCE

```mermaid
flowchart LR
    T[Teacher] --> A[Attendance]
    A --> D{3+ absences?}
    D -->|Yes| F[Follow-up]
    D -->|No| C[Continue]
    F --> P[Parent contact]
```

---

## 5. ESC vs AI TOOLS

| Capability | ChatGPT | Gemini | Gemini Notebook | Perplexity | ESC |
|---|:---:|:---:|:---:|:---:|:---:|
| AI chat | ✓ | ✓ | ✓ | ✓ | ✓ |
| Files | ✓ | ✓ | ✓ | ✓ | ✓ |
| Learning | ✓ | ✓ | ✓ | △ | ✓ |
| Research | ✓ | ✓ | ✓ | ✓ | ✓ |
| Citations | ✓ | ✓ | ✓ | ✓ | ✓ |
| Quiz / revision | ✓ | ✓ | ✓ | △ | ✓ |
| Study planning | ✓ | ✓ | △ | △ | ✓ |
| Specialist agents | △ | △ | △ | △ | **12** |
| Scholarships | — | — | — | — | **✓** |
| Internships / jobs | — | — | — | — | **✓** |
| Teacher communication | — | — | — | — | **✓** |
| Attendance follow-up | — | — | — | — | **✓** |
| Low-data focus | — | — | — | — | **✓** |

```mermaid
flowchart LR
    AI[General AI] --> L[Learn]
    AI --> R[Research]
    ESC[ESC] --> L2[Learn]
    ESC --> P[Plan]
    ESC --> V[Revise]
    ESC --> O[Opportunities]
    ESC --> S[Scholarships]
    ESC --> C[Community]
    ESC --> A[Attendance]
```

---

## 6. 100-TASK BENCHMARK

```mermaid
flowchart LR
    Q[100 Tasks] --> R[25 Research]
    Q --> L[25 Learning]
    Q --> V[20 Revision]
    Q --> P[15 Problem Solving]
    Q --> W[15 Productivity]
```

```mermaid
flowchart LR
    Q[Same Prompt] --> E[ESC]
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

```mermaid
pie title Score Weight
    "Accuracy" : 40
    "Completion" : 30
    "Sources" : 20
    "Instructions" : 10
```

| Tool | Score | Accuracy | Completion | Sources | Latency |
|---|---:|---:|---:|---:|---:|
| ESC | — | — | — | — | — |
| ChatGPT | — | — | — | — | — |
| Gemini | — | — | — | — | — |
| Gemini Notebook | — | — | — | — | — |
| Perplexity | — | — | — | — | — |

---

## 7. ANALYTICS

```mermaid
flowchart TB
    D[Raw Data]
    D --> O[Overall]
    D --> C[Category]
    D --> A[Accuracy]
    D --> L[Latency]
    O --> G1[Chart]
    C --> G2[Chart]
    A --> G3[Chart]
    L --> G4[Chart]
```

---

## 8. ACCESS

```mermaid
flowchart LR
    E[ESC] --> F[Free]
    C[ChatGPT] --> CF[Free + Paid]
    G[Gemini] --> GF[Free + Paid]
    N[Gemini Notebook] --> NF[Free + Paid]
    P[Perplexity] --> PF[Free + Paid]
```

---

## 9. SOURCES

- OpenAI Study Mode
- OpenAI Deep Research
- Google Gemini Help
- Google — Gemini Notebook
- Perplexity Help
- Google One
- Anthropic

## STATUS

`Capability data ✓` · `Benchmark results —`
