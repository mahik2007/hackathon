# ESC --- Data Analytics

### Hackathon-ready • Minimal • Evidence-based

> **Goal:** compare ESC with major AI tools using compact capability
> data + a reproducible benchmark.

------------------------------------------------------------------------

## 1. The Gap

``` mermaid
flowchart LR
    S[Student] --> G[Access gap]
    T[Teacher] --> G
    G --> SCH[Missed scholarships]
    G --> CAR[Low career awareness]
    G --> ATT[Late absence follow-up]
    G --> COM[Scattered communication]
    SCH --> E[ESC Connect]
    CAR --> E
    ATT --> E
    COM --> E
```

  Challenge                 ESC Connect
  ------------------------- --------------------------
  Scattered scholarships    Eligibility + deadlines
  Hidden local careers      Opportunities + channels
  Manual attendance         Follow-up signals
  Scattered communication   School groups

------------------------------------------------------------------------

## 2. Product Map

``` mermaid
flowchart TB
    E[ESC Connect]
    E --> O[Opportunities]
    E --> S[Scholarship Finder]
    E --> C[Academic Community]
    E --> A[Attendance Follow-up]
    O --> O1[Scholarships]
    O --> O2[Internships / Jobs]
    O --> O3[ITI / Careers]
    S --> S1[Profile Match]
    S --> S2[Deadlines]
    C --> C1[Guidance Channels]
    C --> C2[Teacher Groups]
    A --> A1[Absence Signal]
```

------------------------------------------------------------------------

## 3. Core Journey

``` mermaid
sequenceDiagram
    participant P as Student
    participant E as ESC Connect
    participant T as Teacher

    P->>E: Profile
    E-->>P: Matches
    P->>E: Save + checklist
    P->>T: Ask
    T-->>P: Guidance
    T->>E: Attendance
    E-->>T: Follow-up signal
```

------------------------------------------------------------------------

# 4. LLM / AI Tool Comparison

**Legend:** ✓ = documented capability • △ = limited / plan-dependent •
--- = not a core documented focus

  --------------------------------------------------------------------------------
  Capability        ChatGPT       Gemini       Gemini     Perplexity    **ESC**
                                              Notebook                
  --------------- ------------ ------------ ------------ ------------ ------------
  AI chat              ✓            ✓            ✓            ✓            ✓

  PDF / files          ✓            ✓            ✓            ✓            ✓

  Step learning        ✓            ✓            ✓            △            ✓

  Research             ✓            ✓         **Core**     **Core**        ✓

  Source /             ✓            ✓         **Core**     **Core**        ✓
  citations                                                           

  Quiz / practice      ✓            ✓            ✓            △            ✓

  Revision             ✓            ✓            ✓            △            ✓

  Study planning       ✓            ✓            △            △            ✓

  Specialist           △            △            △            △          **12**
  agents                                                              

  Scholarship         ---          ---          ---          ---         **✓**
  matching                                                            

  Internship          ---          ---          ---          ---         **✓**
  discovery                                                           

  Teacher             ---          ---          ---          ---         **✓**
  communication                                                       

  Attendance          ---          ---          ---          ---         **✓**
  follow-up                                                           

  Low-data            ---          ---          ---          ---         **✓**
  education focus                                                     
  --------------------------------------------------------------------------------

### Key analytical distinction

``` mermaid
flowchart LR
    A[General AI] --> B[Answer / Research / Learn]
    C[ESC] --> D[Learn]
    C --> E[Plan]
    C --> F[Revise]
    C --> G[Opportunities]
    C --> H[Scholarships]
    C --> I[Communicate]
    C --> J[Attendance]
```

------------------------------------------------------------------------

# 5. Benchmark Design

``` mermaid
flowchart LR
    P[Same prompt] --> T1[ESC]
    P --> T2[ChatGPT]
    P --> T3[Gemini]
    P --> T4[Gemini Notebook]
    P --> T5[Perplexity]
    T1 --> R[Common rubric]
    T2 --> R
    T3 --> R
    T4 --> R
    T5 --> R
    R --> D[Measured data]
```

### 100-task set

  Category              Tasks
  ----------------- ---------
  Research                 25
  Learning                 25
  Revision                 20
  Problem solving          15
  Productivity             15
  **Total**           **100**

### Score

  Metric             Weight
  -------------- ----------
  Accuracy              40%
  Completion            30%
  Sources               20%
  Instructions          10%
  **Total**        **100%**

> **Do not enter estimated scores.** Fill benchmark results only after
> identical tests.

------------------------------------------------------------------------

# 6. Analytics Output

``` mermaid
flowchart TB
    D[Raw task data] --> S[Overall score]
    D --> C[Category score]
    D --> L[Latency]
    D --> A[Accuracy]
    S --> G1[Overall chart]
    C --> G2[Category chart]
    L --> G3[Latency chart]
    A --> G4[Accuracy chart]
```

### Final measured table

  Tool                Overall   Accuracy   Completion   Sources   Avg. latency
  ----------------- --------- ---------- ------------ --------- --------------
  **ESC**                 ---        ---          ---       ---            ---
  ChatGPT                 ---        ---          ---       ---            ---
  Gemini                  ---        ---          ---       ---            ---
  Gemini Notebook         ---        ---          ---       ---            ---
  Perplexity              ---        ---          ---       ---            ---

------------------------------------------------------------------------

# 7. Access / Pricing Snapshot

  -----------------------------------------------------------------------
  Product                    Free access                   Paid reference
  ----------------- ----------------------------- -----------------------
  **ESC**                         ✓                   No ESC subscription
                                                                    layer

  ChatGPT                         ✓                          Plus \$20/mo

  Gemini                          ✓                     AI Pro \$19.99/mo

  Gemini Notebook                 ✓                 Included in Google AI
                                                      plans with expanded
                                                                   access

  Perplexity                      ✓                   Pro / Education Pro

  Claude                          ✓                 Pro pricing varies by
                                                             current plan
  -----------------------------------------------------------------------

**Important:** this is an access comparison, not a claim that
competitors require payment.

------------------------------------------------------------------------

# 8. Source Data

  -----------------------------------------------------------------------
  Source                              Verified data used
  ----------------------------------- -----------------------------------
  OpenAI Study Mode                   Step-by-step learning, files,
                                      quizzes, flashcard-style review

  OpenAI Deep Research                Multi-step research + sources

  Google Gemini Help                  Deep Research, Search, files, Gmail
                                      / Drive sources

  Google                              NotebookLM renamed **Gemini
                                      Notebook**; research-focused

  Perplexity Help                     Pro Search, multi-source synthesis,
                                      citations, file analysis

  Perplexity Plans                    Free Standard + Pro + Education Pro

  Google One                          AI Pro \$19.99/mo; expanded Gemini
                                      / Gemini Notebook

  Anthropic                           Claude free/pro ecosystem
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# 9. Data Rules

-   Same prompt
-   Same source
-   Same task
-   Same model tier where possible
-   Same rubric
-   Record date
-   Record latency
-   No fabricated scores
-   No subjective winner

**Status:** capability data = documented; benchmark results = pending
measurement.
