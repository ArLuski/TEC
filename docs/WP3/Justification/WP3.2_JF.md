title: |  
  **Gimbal Mount Assembly**  
  Justification File
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
  - \fancyhead[R]{Gimbal Mount Assembly - Justification File - Version 001}
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

# 1. Introduction
## 1.1. Scope  
This document presents the Design Justification File for the Gimbal Mount Assembly (GMA). Its purpose is to explain the rationale behind the selected design and demonstrate that it meets the baseline requirements specified in [RD02]. It lists and describes the justification for:  

- Functional Design
- Thermal Design
- Mechanical Design

##  1.2. Reference
[RD1] A.Lukanowski - Gimbal Mount Assembly - Requirement Consolidation / Version 0 - Luebeck 2026  

[RD02] Gimbal Mount Assembly - Requirement Consolidation / Version 001  


\clearpage

# Functional Design
## Chosen Tolerances and fits
**JUSTIFICATION**
**=>LUG-BEARING: Recommendation by [RD2] and supplier recommendations for rod ends**
**=>Bearing-Bolt dimensions given**
**=>BUSHING-CLEVIS chosen to be clearance fit to ensure precise axial positioning of BEARING innter race**
**SPACER/BUSHING-BOLT clearance fit for flexibiltiy in terms of integration**  
**Show tolerance fit recommendations MIL-Standards, NHBB, RBC, SKF**

## Preload of NAS-bolt

# Thermal Analysis  
**Generic Boundary Conditions**
- Load assumptions
- Convection, Radiation, Conduction

# Mechanical Analysis  
## Bearing Lifetime
  - Show first how size was determined @MIL-HDBK-1599 - 201.143
  - Show computed lifetime according SKF
  - Discuss results
## Bolt, Lug, Clevis
  - Preliminary assesment Ro/Ma
  - Show simplified assumptions and analytical result
  - Show numerical result
## Static Structural  
 ## Prelminary Analysis
  ### Bolt, Lug, Clevis  

  ### Spherical Bearing: Liner Stiffness  

## GMA Static-Structural Analysis
  - 0° with Thrust load and Acceleratoin
  - Worst case angles (pitch/yaw)
  - Discuss results
    - Modelling of liner (boded)

# Conclusion 
\clearpage  


# Annex
## Boundary Conditions Thermal Analysis 

## Boundary Conditions Static Structural Analysis  


\clearpage 
# 3. Acronym List  
The acronyms used in this document are listed below.  

| **Acronym**  | **Definition**   |
|---|---|
|GMA|Gimbal Mount Assembly|

