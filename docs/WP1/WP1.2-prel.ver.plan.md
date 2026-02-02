---
title: |  
  **Gimbal Mount Assembly**  
  Preliminary Verification plan
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
  - \fancyhead[R]{Gimbal Mount Assembly - Requirement Consolidation - Version 001}
  - \renewcommand{\headrulewidth}{0.4pt}
  - \fancyfoot[C]{\thepage}
  - \usepackage{hyperref}
  - 
---
<!--An extension to these requierements are given in a Excel named "Huracan-TVC-Preliminary-Spec.xlsx" created by Pierre Vinet -->

\pagenumbering{roman}
\setcounter{page}{1}
\tableofcontents
\clearpage
\pagenumbering{arabic}

# Introduction
This document shows the preliminary verification method and plan of the Gimbal Mount Assembly (GMA) and reflects the
status of the development associated to the requirement consolidation [RD1]. The main objective is to demonstrate that the product meets the specified requirements considering the resources, capabilities, costs and schedule of the The Exploration Company (TEC).

## Compliance Statuses  
The following compliance statuses are used:

- **C** (Compliant): the requirement is considered applicable and is implemented in the design

- **NA** (Not Applicable): the requirement is considered not applicable to the system (e.g. berthing-related requirements are not applicable to a docking vehicle.)

- **T** (Tailored): the requirement is not fulfilled to its full extent. The compliance comment will indicate the limitations.

- **NC** (Not Compliant): the requirement, although considered applicable, is not taken into account in the design.


## Reference
[RD1] Gimbal Mount Assembly Requirement Consolidation - Version 0

[RD2] Space engineering - Verification - ECSS-E-ST-10-02C Rev.1 01.02.2018

\clearpage

# Definitions

## Shall  
The use of "shall" in this document defines a requirement, which must be verified considering the proposed level and
the proposed method.  

## Units  
All quantitative values shall be provided in SI units  

## Language
All notices, documents, deliverables and other communications between the main parties, including by their respective
employees and related Third Parties shall be in English.

## Verification Methods
The verification methods utilized for the development of the GMA are closely associated to The Exploration Companies verification policy and ECSS-standard [RD2]: Review of Design, Analysis, Inspection and Test.

### RoD: Review of Design  
This is typically a review of the as-built drawings to confirm that a design feature has been incorporated into the
design. It also includes reviews of design documents like the definition-, justification file, interface control documents and engineering drawings.

### A: Analysis  
Verification by analysis shall contain theoretical evaluation of the design. Techniques like qualitative design assesments, modelling and computatuional simulation (e.g. FEM) and similarity assessments describe this verification method. Analytical methods selected for verification shall be supported by appropriate rationale and detailed documentation (assumptions, limitations, uncertainties). Analysis covers also the evaluation of empirical data that can be provided by the customer (tests or validated analysis), investigations for similar designs or heritage.  

### I: Inspection  
Inspection verifies physical characteristics that determine compliance of the item with requirements normally without the use of special laboratory equipment, procedures, test support items, or services. Standard methods and tools are utilized for inspection such as visual assessment, gauges, etc., to verify compliance with the requirements. Hardware may be inspected for the following:
- Construction
- Workmanship
- Physical condition
- Specification and/or drawing compliance
  
Inspection may be used to confirm that engineering drawings call out proper design and construction features (e.g.,tolerances
materials, processes). Inspection does NOT include Review of Design (ROD).  

### T: Test  
Test is a method of verification wherein requirements are verified by measurement during or after the controlled
application of functional and environmental stimuli. These measurements may require the use of laboratory equipment, recorded data, procedures, test support items, or services. For all verification, qualification, and acceptance test activities, pass or fail test criteria or acceptance tolerance bands (based upon design and performance requirements)
shall be specified before conducting the test. This will ensure that the actual performance of tested equipment or systems meets or exceeds specifications.

# Gimbal Mount Assembly


# Acronym List  
The acronyms used in this document are listed below.  

| **Acronym**  | **Definition**   |
|---|---|
|IH|Injection Head flange|
|GMA|Gimbal Mount Assembly|
|PCD|Pitch Circle diameter|
|QSL|Quasi-static load|
|TEC|The Exploration Company|
