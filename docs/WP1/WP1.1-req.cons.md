---
title: |  
  **Gimbal Mount Assembly**  
  Requirement Consolidation
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
Based on the preliminary requirements initially shared by The Exploration Company (TEC) for this activity [RD1], this document refines the key performance parameters. These updated requirements primarily relate to the Hopper Ground Demonstrator *Oneiros*, which is also part of a de-risking activity for the *Huracan* propulsive system [RD2]. During the development of the Gimbal Mount Assembly (GMA), the focus will be on prioritizing *Oneiros* requirements, while also considering intentions for upcoming design iterations of the *Huracan* engine and its components. 

##  1.2. Reference
[RD1] Consultant Agreement 12.12.2025 - Docusign Envelope ID: AA5722EA-0E20-45A6-BFE2-2B6D313A7FF3

[RD2] Design Description and Justification File - TEC-ITA-DOC-2025-01011 - Version 3

[RD3] System Requirements Document - TEC-ITA-DOC-2025-01017 - Version 0

[RD4] Modern Engineering for design of liquid propelleant rocket engines - D.Huzel / D.Huang, Vol. 147, p. 341

\clearpage

# 2. Requirements

## 2.1. Environmental requirements  

**REQ-033 - Pollution requirements**  

Sensitive areas, such as regions of relative motion, shall be protected against sand particles with an average size of 0.2 mm at a temperature of 49.6 °C [RD3].  
________________________

**REQ-020 - Ambient requirements**  

According to the system requirements of *Oneiros*, the sea level conditions are defined by a pressure of 0.994 bar to 1.0276 bar and 12 % to 91 % humidity. The ambient temperature ranges from 8.3 °C to 49.6 °C. [RD3]  

## 2.2. Functional requirements

**REQ-003 - Operational gimbal capability** 

The GMA design provides an operational deflection capability of ±10° per axis (pitch and yaw), which covers the GNC needs as well as the mechanical limits of the subsystem and its components (e.g., bellows and actuators).  
________________________

**REQ-034 - Max. gimbal capability**  

For off-nominal cases and emergency authority, the max. gimbal angle shall not exceed +/-12 °.   
________________________

**REQ-002 - Rotation axis**  

To provide full pitch and yaw control capability, a two-axis rotation mechanism shall be implemented. Both axes are positioned perpendicular to each other within the same horizontal plane.
________________________

**REQ-004 - Angular velocity**  

To compromise GNC needs with mechanical constraints of the engine such as the actuator capacity, the max. angular velocity of the engine is 20 °/s.  
________________________

**REQ-005 - Angular acceleration**  

The engine´s acceleration and hence, the capability of the GMA shall be max. 25 rad/s².  
________________________

**REQ-0014 - Mass**   

The maximum mass of the GMA shall be equal or below 5 kg with a measurement accuracy of +/-0.1 %.  
________________________

**REQ-013 - Geometrical envelope**  

A damage- and collision-free motion under worst case angle conditions is required between the Igniter´s main body (incl. it´s attachments) and the GMA geometry. A minimum clearance of 20 mm is to be considered between moving parts. The maximum geometrical limit of th GMA is given by the mass constraint, the loads and (thermo-)mechanical stress requirements mentioned in this document. The Ignition System´s main body (Ø70 mm) is designed with a vertically offset of 63 mm from the Injection Head (IH) upper flange surface.  
________________________

**REQ-015 - Geometrical interface**  

For the lower attachment of the GMA, the utilizable surface of the IH features a ring with an inner diameter of Ø100 mm and an outer diameter of Ø170 mm. In total, eight through-holes (Ø9 mm each) are available, spaced at 45° intervals (symetrically along PCD). Eight M8 fasteners are intended to fix the GMA with the IH (minimum tensile ultimate strength per fastener: 800 MPa). 

## 2.3. Mechanical and thermal requirements   

**REQ-016 - Max. payload**  

The gimbal will be designed to support a maximum payload mass of 40 kg, corresponding to the Thrust Chamber Assembly (TCA) plus margins of the cryogenic engine.  
________________________  

**REQ-018 - Friction coefficient**  

To reduce the breaking torque of the actuators, the GMA shall provide a constant friction coefficient equal or lower than 0.1 under mechanical and thermal operating conditions.  
________________________

**REQ-008 - Plastic Deformation and crack formation**  

The GMA and its parts shall not undergo plastic deformation, crack formation or other non-recoverable deformation when subjected to the operational conditions defined in this specification. Exceptions can be permissible if non-recoverable deformation is identified as a single, local phenomena, that occurs in extraordinary or single event load case. In this case the non-recoverable deformation is to be justified by analysis at least.  
________________________

**REQ-001 - Operating nominal thrust**  

The GMA shall transmit a total nominal thrust load of 15 kN. 
<!-- Formulation rather generic for future flexibility and adaptation like. 15 kN under worst case gimbal angle conditions might overconstraint the GMA-->  
________________________

**REQ-039 - Quasi-Static Load (QSL)**  

For single events, the GMA shall sustain an excessive thrust load of 22.5 kN at gimbal angle of 0 °, which includes a safety factor of 1.5 applied to the nominal thrust.  
________________________

**REQ-021 - Mechanical and thermal transient**  

Until steady state conditions are achieved, transient conditions dominate. A cooling from ambient 280 K to 180 K within 10 s is to be considered linearly, with a slope of 10 K/s. This is to be taken into account at the GMA surface, that is connected to the IH upper flange. A chamber overpressure rate of 210 bar/s is to be anticipated for a transinent occasion.
<!--280K (ambient) was measured at DLR. For Oneiros it might be higher as almost 50°C can be targeted for ambient tests at UAE. Also,
the lower temperature of 180K might be incerased under these ambient conditions. TBD! -->    
________________________

**REQ-020 - Operating temperature**  

An operating temperature of 120 K to 150 K shall be considered at the IH top flange surface that is connected to the GMA support.
<!--For testing of Oneiros, ambient temperatures of almost 50°C may increase the operating temperatures. TBC! -->  
________________________  


**REQ-030 - Cycling**  

The GMA shall sustain a minimum of 1000 cycles, which is derived from preliminary GNC-data.  
________________________  


## 2.4. Growth potential requirements

**REQ-035 - Extended cycling**  

For further utilization of the GMA for flight qualification and preperation for the moon mission, 26520 cycles are targeted.  
________________________  

**REQ-036 - Lateral misalignment**  

The GMA shall contain features to compensate lateral misalignment of the thrust vector up to +/-10 mm [RD4].  
________________________  

**REQ-037 - Vacuum environment**  

The GMA performance in ambient conditions shall be adapted to operate feasibly in vacuum, especially concerning lubrication, thermal and mechanical loads. 

\clearpage

# 3. Acronym List  
The acronyms used in this document are listed below.  

| **Acronym**  | **Definition**   |
|---|---|
|IH|Injection Head flange|
|GMA|Gimbal Mount Assembly|
|PCD|Pitch Circle diameter|
|QSL|Quasi-static load|
|TEC| The Exploration Company|
