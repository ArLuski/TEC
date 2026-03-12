---
title: |  
  **Gimbal Mount Assembly**  
  Trade-Off Report
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

[RD2] A.Lukanowski - Gimbal Mount Assembly - Preliminary Verification Control Document / Version 0 - Luebeck 2026

[RD3] ECSS-E-ST-10C Rev.1 - System engineering general requirements

[RD4] T.L. Saaty - Decision Making for Leaders: The Analytic Hierarchy Process for Decision in a Complex World - Pittsburgh 1990

[RD5] D.Huzel, D.Huang - Modern Engineering For Design Of Liquid-Propellant Rocket Engines - Washington 1992

[RD6] A.Lukanowski - 20260310_Luka_GMA_Tradeoff_AHP / Excel file - Luebeck 2026

[RD7] P.Vinet - NYX Moon - Huracan Development Logic - TEC-FRA-DOC-2024-01004 - Bordeaux 2024

\clearpage

# 2. Trade-Off 

## 2.1. Philosophy and criteria

The trade-off philosophy for this specific use case is to have a design that is *safe, simple and achievable* within the time frame. This philosophy is given by the low TRL of the GMA in the current project state (here: TRL 1/2) and programmatic constraints (e.g. delivery of a functional model before DM2). The objective is to deliver a functional model on schedule by keeping it as simple as possible and only as complex as necessary considering technical feasibility constraints.

**Program criteria**  
  Programmatic aspects are associated to "The How and When"-question, which shall address the lifecycle, constraints and hence the success of the project. For this project, the focus of this criteria is mainly the schedule (timeline, lead time), execution (supply chain / manufacturing) and testability. 

**Functional criteria**  
  The functional criteria refer to the question "What?", which is linked to the control authority needs. Those key performance requirements [RD1] are the gimbal angle, angular speed and precision. In addition, the mass requirement is directly associated to the overall mass budget, while the volume envelops the geometrical constraint to fullfill the key requirements (e.g. clearance vs. gimbal angle) and the integration. 

**Feasibility criteria**  
  The "If"-question is covered by feasability aspects, which refer to technical risks reduction, related to its Technology Readyness Level (TRL), the design complexity (part count, tolerance sensitivity etc.) and its load capability (thermal and mechanical).
  
## 2.2. Methodology

The trade-off is performed by using the methodology of the Analytic Hierarchy Process (AHP) [RD4], combined with an subsequent decision matrix. The methodology of AHP helps to evaluate criteria by breaking problems into a hierarchy of simpler elements. It covers the following steps:

1. Structuring the problem into a hierarchy with objectives, criteria and sub-criteria
2. Pairwise comparison and weighting of the criteria.
3. Ranking alternatives based on the overall scores to aid in selecting the best option

For this trade study, the weights derived from the AHP are taken as input for the decision matrix. In this decision matrix, several design options will be weighted against each other based on the criteria coming from the AHP. The outcome shall be a suggestion for a final concept design. 

## 2.3. Analytic Hierarchy Process (AHP)

For this study, an AHP-template was utilized that is annexed in the delivery package of this document [RD6]. The fundamental scale values of the AHP are shown in the figure below. 

![AHP scale [RD6]](figures/20260311_Luka_Trade-Off_AHP_Scale.png){width=30%}

Considering the trade-off philosophy *"safe, simple, achievable"*, the scaling values are assigned to 8 criteria in the AHP as shown in the subsequent figure.

![Pairwise Comparison Matrix [RD6]](figures/20260311_Luka_Trade-Off_AHP_Pairwise Comparison Matrix.png)

The computed plausibility of the assignment is given by a consistency of 4 % (<10 % for successful consistency). The resulting rankings of the criteria are:

The AHP weights and rankings are shown in the table below. 

|**Criteria**|**AHP**|**Ranking**|
|---|---|---|
|Timeline & Execution|15.1 %|3|
|Testability|28.7 %|1|
|**PROGRAMMATIC total**|**43.8 %**|**1**|
||||
|Angle, speed, precision|7.8 %|6|
|Mass|3.4 %|8|---|
|Geometry / Volume|4.1 %|7|
|**FUNCTIONALITY total**|**15.2 %**|**3**|
||||
|TRL|20.6 %|2||3|
|Complexity|11.3 %|4|
|Load capability|9.1 %|5|
|**FEASIBILITY total**|**41 %**|**2**|
: Criteria, AHP and Ranking

With a total weight of 43.8 %, programmatic criteria represent the most influential category. In particular, the need for testability accounts for 28.7 % of the overall decision model and therefore constitutes the single most dominant criterion.

The second most influential factor is the TRL, which acts as the primary feasibility driver with a weight of 20.6 % (Rank 2). In contrast, functional performance represents a secondary optimization layer. Although its overall contribution (15.2 %) is comparatively small, it cannot be fully neglected in the decision process.

The weighting indicates that the development strategy clearly prioritizes risk reduction through verification and validation approaches. Consequently, complex or low-TRL but innovative concepts will only remain competitive if they provide significant advantages in other areas and are supported by a strong analytical justification.

The results further suggest that heavier solutions with a larger geometrical envelope or non-optimal performance margins may still be selected, provided that they are easily testable, exhibit an acceptable maturity level (minimum TRL 4), and can be delivered within the required development timeline.

Regarding complexity (11.3 %, Rank 4), the results indicate that more complex designs are acceptable as long as they maintain sufficient maturity and remain compatible with feasible verification approaches.

Overall, the weighting generated by the AHP analysis aligns well with the philosophy intentions mentioned above, emphasizing programmatic reliability and technological maturity over purely performance-driven optimization.

## 2.4. Design options
Several methods exist for Thrust Vector Control Systems (TVC) of a vehicle. Some examples are auxiliary jets, secondary injection or a gimbaled engine [RD5]. The focus in this study is the gimbaled engine option as it is the most common used one. It consists of a gimbal mechanism, that provides the rotational degree of freedom in two perpendicular axes (pitch and yaw) and two actuators, which power the engine´s movement. Three main GMA options are described briefly by their geometrical type.

**Ring-type**  
A classical Ring-type GMA design is shown below. It typically consists of a lower support structure that is typically attached on the top of the Injection Head (IH). A gimbal ring interfaces this lower structure with an upper structure, that is connected with the thrust frame of the vehicle. The rotational degree of freedom is realized by four bearings, which are clocked in a 90° arrangement. This design is widely used in sovjet engines, where the propellant-duct passes through the core (vertical) axis of the gimbal respectively engine.  

![Ring-type GMA [RD5]](figures/20260311_Luka_Trade-Off_Ring_type gimbal.png){width=37%}

**Cross-type**  
The ring-type GMA described above is related to the cross-type design. The main difference is the compactness and stiffness benefits of the cross-type as it features no capability to pass through a propellant-duct. The bearings inner races are supported by an monolithc cross-shaped bolt unit (also clocked by 90°). The outer races of the bearings are connected to an lower and upper retainer or housing in analogy to the lower and upper support of the ring-type GMA. The figure below illustrates the cross-type GMA exemplarily as it was developed for the VINCI upper stage engine. 

![Cross-type GMA developed for VINCI](figures/20260311_Luka_Trade-Off_Cross-type gimbal.png){width=37%}

**Spherical-type**  
The spherical-type of GMA provides the highest load capability combined with a compact design. It consists of a lower / upper flange, that is connected to the engine / vehicle. The gimbal mechanism features a ball-and socket joint with convex and concave spherical surfaces that are interfaced by an Teflon-fiber-glass composite to provide maintanance-free and low friction relative motion. The image below shows a spherical-type GMA as it was / is utilized for the RS-25 and Vulcain 2 core stage engine. 

![Spherical-type GMA [RD5]](figures/20260311_Luka_Trade-Off_Spherical-type gimbal 2.png){width=60%}

## 2.5. Decision matrix

## 2.6. Conclusion and final concept
Three different concepts exist in rocketry for gimbal mechanisms:
- Ring type
- Spherical type
- Cross type
- Other

\clearpage

# 3. Acronym List  
The acronyms used in this document are listed below.  

| **Acronym**  | **Definition**   |
|---|---|
|AHP|Analytic Hierarchy Process|
|DM2|Development Model 2|
|GMA|Gimbal Mount Assembly|
|IH|Injection Head flange|
|TRL|Technology Readiness Level|
|TVC|Thrust Vector Control|