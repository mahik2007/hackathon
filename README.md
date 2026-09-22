# ESC — Data Analytics

## 01 · GAP

```mermaid
flowchart LR
S[Student] --> G[ACCESS GAP]
T[Teacher] --> G
G --> A[Scholarship]
G --> B[Career]
G --> C[Attendance]
G --> D[Communication]
A --> E[ESC CONNECT]
B --> E
C --> E
D --> E
```

| Problem | Module |
|---|---|
| Scholarships | Finder |
| Jobs / ITI | Opportunities |
| Absence | Follow-up |
| Communication | Community |

---

## 02 · ESC CONNECT

```mermaid
flowchart TB
E[ESC CONNECT]
E --> O[OPPORTUNITIES]
E --> S[SCHOLARSHIPS]
E --> C[COMMUNITY]
E --> A[ATTENDANCE]
O --> O1[Jobs]
O --> O2[Internships]
O --> O3[ITI]
S --> S1[Profile]
S --> S2[Match]
S --> S3[Deadline]
C --> C1[Teacher]
C --> C2[Student]
A --> A1[Absence]
A --> A2[Follow-up]
```

## 03 · STUDENT FLOW

```mermaid
flowchart LR
P[Profile] --> M[Match] --> V[View] --> S[Save] --> R[Reminder] --> A[Apply]
```

```mermaid
sequenceDiagram
S->>E: Profile
E-->>S: Match
S->>E: Save
S->>T: Ask
T-->>S: Guidance
```

---

## 04 · ATTENDANCE

```mermaid
flowchart LR
T[Teacher] --> A[Attendance] --> D{3+?}
D -->|Yes| F[Follow-up]
D -->|No| C[Continue]
F --> P[Parent]
```

---

## 05 · CAPABILITY MATRIX

| Capability | ChatGPT | Gemini | Notebook | Perplexity | **ESC** |
|---|:---:|:---:|:---:|:---:|:---:|
| Chat | ✓ | ✓ | ✓ | ✓ | ✓ |
| Files | ✓ | ✓ | ✓ | ✓ | ✓ |
| Learning | ✓ | ✓ | ✓ | △ | ✓ |
| Research | ✓ | ✓ | ✓ | ✓ | ✓ |
| Citations | ✓ | ✓ | ✓ | ✓ | ✓ |
| Quiz | ✓ | ✓ | ✓ | △ | ✓ |
| Revision | ✓ | ✓ | ✓ | △ | ✓ |
| Planning | ✓ | ✓ | △ | △ | ✓ |
| **12 agents** | — | — | — | — | **✓** |
| Scholarships | — | — | — | — | **✓** |
| Jobs / ITI | — | — | — | — | **✓** |
| Teacher chat | — | — | — | — | **✓** |
| Attendance | — | — | — | — | **✓** |
| Low-data focus | — | — | — | — | **✓** |

```mermaid
flowchart LR
G[GENERAL AI] --> L[Learn]
G --> R[Research]
E[ESC] --> L2[Learn]
E --> P[Plan]
E --> V[Revise]
E --> O[Opportunity]
E --> S[Scholarship]
E --> C[Community]
E --> A[Attendance]
```

---

## 06 · 12 AGENTS

```mermaid
flowchart TB
E[ESC]
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

---

## 07 · BENCHMARK

```mermaid
flowchart LR
Q[100 TASKS]
Q --> R[25 Research]
Q --> L[25 Learning]
Q --> V[20 Revision]
Q --> P[15 Problems]
Q --> W[15 Productivity]
```

```mermaid
flowchart LR
Q[Same Tasks] --> E[ESC]
Q --> C[ChatGPT]
Q --> G[Gemini]
Q --> N[Notebook]
Q --> P[Perplexity]
E --> R[Same Rubric]
C --> R
G --> R
N --> R
P --> R
```

| Metric | Weight |
|---|---:|
| Accuracy | 40% |
| Completion | 30% |
| Sources | 20% |
| Instructions | 10% |

```mermaid
pie title Benchmark Weight
"Accuracy" : 40
"Completion" : 30
"Sources" : 20
"Instructions" : 10
```

---

## 08 · RESULTS

| Tool | Score | Accuracy | Completion | Sources | Latency |
|---|---:|---:|---:|---:|---:|
| ESC | — | — | — | — | — |
| ChatGPT | — | — | — | — | — |
| Gemini | — | — | — | — | — |
| Notebook | — | — | — | — | — |
| Perplexity | — | — | — | — | — |

```mermaid
flowchart TB
D[Raw Data] --> S[Score]
D --> A[Accuracy]
D --> C[Completion]
D --> L[Latency]
S --> G1[Overall]
A --> G2[Accuracy]
C --> G3[Completion]
L --> G4[Latency]
```

---

## 09 · ACCESS

| Tool | Free | Paid |
|---|:---:|:---:|
| ESC | ✓ | — |
| ChatGPT | ✓ | ✓ |
| Gemini | ✓ | ✓ |
| Notebook | ✓ | ✓ |
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

## 10 · DATA SOURCES

| Source | Data |
|---|---|
| OpenAI | Study Mode + Deep Research |
| Google | Gemini + Notebook |
| Perplexity | Search + citations |
| Anthropic | Claude |

---

### STATUS

`Data ✓` · `Benchmark —`
