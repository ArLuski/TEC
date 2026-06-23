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

# 1. Introduction
## 1.1. Scope
This document presents the Gimbal Mount Assembly (GMA) Trade-Off Report. The objective of this file is to support the concept design decision among alternative solutions taking into account technical and programmatic constraints. 

##  1.2. Reference
[RD1] A.Lukanowski - Gimbal Mount Assembly - Requirement Consolidation / Version 0 - Luebeck 2026

[RD2] BEARINGS, CONTROL SYSTEM COMPONENTS, AND ASSOCIATED
HARDWARE USED IN THE DESIGN AND CONSTRUCTION OF
AEROSPACE MECHANICAL SYSTEMS AND SUBSYSTEMS / MIL-STD-1599 


\clearpage

# 2. Tolerances and fits
**JUSTIFICATION**
**=>LUG-BEARING: Recommendation by [RD2] and supplier recommendations for rod ends**
**=>Bearing-Bolt dimensions given**
**=>BUSHING-CLEVIS chosen to be clearance fit to ensure precise axial positioning of BEARING innter race**
**SPACER/BUSHING-BOLT clearance fit for flexibiltiy in terms of integration**


## 2.1. blabla


# 3. Acronym List  
The acronyms used in this document are listed below.  

| **Acronym**  | **Definition**   |
|---|---|
|GMA|Gimbal Mount Assembly|

