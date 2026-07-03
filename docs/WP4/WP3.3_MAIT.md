---
title: |  
  **Gimbal Mount Assembly**  
  Manufacturing, Assembly, Integration and Test Plan
author: Artjom Lukanowski on behalf of The Exploration Company SAS     
version: "001"
date: "Version 001 created on \\today"
output:
  pdf_document:
    toc: true
    toc_depth: 3

header-includes:
  - \usepackage{titling}
  - \renewcommand{\maketitle}{
      \begin{titlepage}
        \thispagestyle{empty}
        \vspace*{\fill}
        \begin{center}
          {\huge\normalfont \thetitle\par}
          \vspace{2em}
          {\normalsize\normalfont \theauthor\par}
          \vspace{1em}
          {\normalsize\normalfont \thedate\par}
        \end{center}
        \vspace*{\fill}
      \end{titlepage}
    }
  - \usepackage[a4paper,left=20mm,right=20mm,top=25mm,bottom=25mm]{geometry}
  - \usepackage{fancyhdr}
  - \fancyhead[L]{\nouppercase{\leftmark}}
  - \pagestyle{fancy}
  - \fancyhf{}
  - \fancyhead[R]{Gimbal Mount Assembly - Manufacturing, Assembly, Integration and Test Plan - Version 001}
  - \renewcommand{\headrulewidth}{0.4pt}
  - \fancyfoot[C]{\thepage}
  - \usepackage{hyperref}
  - 
---
\pagenumbering{roman}
\setcounter{page}{1}
\clearpage
\pagenumbering{arabic}

# 1. Introduction
## 1.1. Scope  
The purpose of the Manufacturing, Assembly, Integration and Test (MAIT) Plan is to describe the
 MAIT process and demonstrate together with the verification plan how the requirements are verified by
inspection and test.
It contains the overall Manufacturing, AIT activities, suggestions for associated verification tools (GSE and facilities) and the involved documentation.

## 1.2. Reference  

[RD1] Gimbal Mount Assembly - Definition File / Version 001 

[RD2] Nyx Moon - Huracan Overall Test Plan / TEC-FRA-DOC-2024-01005 / Issue: 1


\clearpage
 

# GMA Presentation  

....

# Manufacturing  

The manufacturing process shall follow the companies proven internal processes from sourcing of the raw material until final manufacturing


## Overview of materials and proceses  

....

## Heat Treatment  

....  

## CNC machining  

...  

# Assembly  

## Required Tools  

...  

## Assembly Sequence  

...  Exploaded view and assembly sequence  
... Torques for bolted joints

# Integration  

... Describe Integration with engine  
... Torques for bolted joints

# Test  

All GMA is subjected to a verification programme appropriate to their development status and intended use. In accordance with common ECSS and NASA terminology, the tests are grouped into three main categories:
  
- Acceptance Tests
- Development Tests
- Qualification Tests

**Acceptance** tests are performed on each manufactured part to verify conformity, workmanship, structural integrity, and basic functionality before assembly to a component and higher-level engine system testing later. 

Following successful component acceptance, the hardware proceeds to engine-level testing. **Development** tests support design maturation, characterization, and the resolution of technical issues. **Qualification tests** are performed on a controlled, flight-representative configuration to demonstrate compliance with the specified performance, durability, structural, and safety requirements.

The following chapters describe the objectives, scope, methods, and acceptance criteria for each test category.

## Acceptance Test

### Inspection  

**Inspection prior engine operation**

**Inspection after engine operation** 

**Success criteria**

### Functional Tests  

## Development Test  

Development tests are conducted during the design-maturation phase to build confidence in new designs and concepts aligned with the Overall Test Plan objectives on the engine system level in accordance to [RD2]. Their objectives are to:

- Characterize the behaviour and performance of the engine;
- Identify weaknesses in the materials, components, interfaces, or overall design;
- Validate and correlate analytical models;
- Investigate operating limits and off-nominal behaviour;
- Support the resolution of design issues; and
- Provide confidence that the final design can successfully complete qualification.

Development-test conditions can extend beyond the normal design or operating range where this is necessary to identify credible weaknesses or design deficiencies. Development testing is iterative and can be performed concurrently with design modifications. However, successful development testing does not, by itself, constitute qualification unless the test article, configuration, test levels, durations, instrumentation, procedures, and success criteria satisfy all applicable qualification requirements.
  
## Qualification Test  

Qualification testing is performed after the design has reached a controlled and sufficiently mature configuration. It is conducted on a dedicated qualification engine or other approved flight-representative engine to demonstrate that the design complies with its specified requirements in the intended operational environments, including the applicable qualification margins. It is assumes that the objectives of the Qualification Tests are defined and executed at engine system level. Hence, the objectives are ellaborated in the Huracan Overall Test Plan [RD2]

# AIT documentation  

Assembly and acceptance tests procedures shall be written and executed using a system with version control capability.  

Non-conformances shall be documented and tracked in the TEC-internal ERP system and evaluated together with the quality engineers.


\clearpage

# 4. Acronym  

| **Acronym**  | **Definition**   |
|---|---|
|GMA  |Gimbal Mount Assembly|
|MATI |Manufacturing, Assembly, Integration and Test|
: Acronyms

