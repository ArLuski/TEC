---
title: |  
  **Gimbal Mount Assembly**  
  Preliminary Verification Control Document
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
  - \fancyhead[R]{Gimbal Mount Assembly - Prel. Verification Control Document - Version 001}
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
This document shows the preliminary verification method and plan of the Gimbal Mount Assembly (GMA) and reflects the
status of the development associated to the requirement consolidation [RD01]. The main objective is to demonstrate that the product meets the specified requirements considering the resources, capabilities, costs and schedule of this project.

## 1.1. Compliance Statuses  
The following compliance statuses are used:

- **C** (Compliant): the requirement is considered applicable and is implemented in the design

- **NA** (Not Applicable): the requirement is considered not applicable to the system (e.g. berthing-related requirements are not applicable to a docking vehicle.)

- **T** (Tailored): the requirement is not fulfilled to its full extent. The compliance comment will indicate the limitations.

- **NC** (Not Compliant): the requirement, although considered applicable, is not taken into account in the design.


## 1.2. Reference
[RD01] Gimbal Mount Assembly - Requirement Consolidation / Version 0

[RD02] Space engineering - Verification / ECSS-E-ST-10-02C Rev.1 / 2018

[RD03] Huracan - TCA Interface Control Document / TEC-FRA-DOC-202401143 / Version 1

[RD04] Modern Engineering for design of liquid propelleant rocket engines - D.Huzel / 1992

\clearpage

# 2. Definitions

## 2.1. Shall  
The use of "shall" in this document defines a requirement, which must be verified considering the proposed level and
the proposed method.  

## 2.2. Units  
All quantitative values shall be provided in SI units  

## 2.3. Language
All notices, documents, deliverables and other communications between the main parties, including by their respective employees and related ThiRD0 Parties shall be in English.  

## 2.4. Verification Methods
The verification methods used for the development of the GMA are closely aligned with The Exploration Company’s (TEC) verification policy and the ECSS standaRD0 [RD02]: *Review of Design, Analysis, Inspection, and Test*. Verification shall be carried out using one or more of these methods.

### 2.4.1. RoD: Review of Design  
This is typically a review of the as-built drawings to confirm that a design feature has been incorporated into the
design. It also includes reviews of design documents like the definition-, justification file, interface control documents and engineering drawings.

### 2.4.2. A: Analysis  
Verification by analysis shall contain theoretical evaluation of the design. Techniques like qualitative design assesments, modelling and computatuional simulation and similarity assessments describe this verification method. Analytical methods selected for verification shall be supported by appropriate rationale and detailed documentation (assumptions, limitations, uncertainties). Analysis covers also the evaluation of empirical data that can be provided by the customer (tests or validated analysis), investigations for similar designs or heritage.  

### 2.4.3. I: Inspection  
Inspection verifies physical characteristics that determine compliance of the item with requirements normally without the use of special laboratory equipment, procedures, test support items, or services. StandaRD0 methods and tools are utilized for inspection such as visual assessment, gauges, etc., to verify compliance with the requirements. HaRD0ware may be inspected for the following:
- Construction
- Workmanship
- Physical condition
- Specification and/or drawing compliance
  
Inspection may be used to confirm that engineering drawings call out proper design and construction features (e.g.,tolerances
materials, processes). Inspection does NOT include Review of Design (ROD).  

### 2.4.4. T: Test  
Test is a method of verification wherein requirements are verified by measurement during or after the controlled
application of functional and environmental stimuli. These measurements may require the use of laboratory equipment, recoRD0ed data, procedures, test support items, or services. For all verification, qualification, and acceptance test activities, pass or fail test criteria or acceptance tolerance bands (based upon design and performance requirements)
shall be specified before conducting the test. This will ensure that the actual performance of tested equipment or systems meets or exceeds specifications.

# 3. Preliminary Verification Control Document  

## 3.1. Environmental requirements  

**REQ-033 - Pollution requirements**  
*Sensitive areas, such as regions of relative motion, shall be protected against sand particles with an average size of 0.2 mm at a temperature of 49.6 °C.*  

Verification method(s):  

- **I**: The absolute temperature of the sand located near the vehicle launch area shall be measured prior to launch using a calibrated temperature sensor (e.g., soil thermometer). Average particle size shall be assessed by measuring ten randomly selected sand particles using a caliper. The investigation shall be accompanied by appropriate documentation of ambient environmental conditions, including air temperature, relative humidity, atmospheric pressure, and wind speed.  

________________________

**REQ-020 - Ambient requirements**  
*AccoRD0ing to the system requirements of *Oneiros*, the sea level conditions are defined by a pressure of 0.994 bar to 1.0276 bar and 12 % to 91 % humidity. The expected ambient temperature range is 8.3 °C to 49.6 °C.*  
 
Verification method(s): 

- **I / T**: The absolute ambient temperature is to be measured with simple instrumentation like a thermometer (RTDs) or thermistor. The environmental pressure can be measured by a barometer (mechanical or electronic pressure sensor). A hygrometer measures relative humidity. Digital sensors (capacitive or resistive) are common. All values are to be referenced and documented w.r.t the local meteorological station´s measurements.  

________________________

## 3.2. Functional requirements  

**REQ-003 - Operational gimbal capability**  

*The GMA design provides an operational deflection capability of ±10° per axis (pitch and yaw), which covers the GNC needs as well as the mechanical limits of the subsystem and its components (e.g., bellows and actuators).*  

Verification method(s):  

- **A**: A kinematic analysis in CAD shall prove the gimbal capability on a component and system level of the entire engine, including ducts, actuators etc.  

- **I**: Prior to assembly of the GMA it´s deflection angles are to be measured, e.g. by marking. From the neutral position (gimbal angle 0 °), the deflection up to +/-10 ° for pitch and yaw is to be determined. Also, the *corner-deflection* is to be documented with combined pitch and yaw deflections (e.g. pitch: +10 °C / yaw: +10 °C; pitch +10 °C / yaw: -10 °C etc.).  

________________________

**REQ-034 - Max. gimbal capability**  

*For off-nominal cases and emergency authority, the max. gimbal angle shall not exceed +/-12 °.*  

Verification method(s):  

see REQ-003 - Operational gimbal capability  

________________________

**REQ-002 - Rotation axis**  

*To provide full pitch and yaw control capability, a two-axis rotation mechanism shall be implemented. Both axes are positioned perpendicular to each other within the same horizontal plane.*  

Verification method(s):  

- **RoD, A**: Analysis of tolerances based on manufacturing drawings and quality reports shall be utilized for post-machined investigations. 

- **I**: For inspection, the measurement of the perpendicularity of both axis may be done by reference planes with simple gauges like a precision square under ambient and unloaded conditions. This is to be realized for the entire angle range of the gimbal for pitch and yaw.  

________________________  

**REQ-004 - Angular velocity**  

*To compromise GNC needs with mechanical constraints of the engine such as the actuator capacity, the max. angular velocity of the engine is 20 °/s.*  

Verification method(s):  

- **A**: A kinematic analysis shall be executed to determine the angular velocity based on the translational velocity of the actuators and the moving mass. 

- **T**: The angular velocity can be computed by speed sensor measurements. A proper instrumentation is to be chosen to account for operational constraints (e.g. temperature, vibration).  

________________________

**REQ-005 - Angular acceleration**  

*The engine´s acceleration and hence, the capability of the GMA shall be max. 25 rad/s².*  

Verification method(s):  

- **A**: A kinematic analysis is to be executed to determine the angular acceleration based on the translational acceleration of the actuators. 

- **T**: The angular acceleration can be mathematically derived through signal processing from angular velocity measurements (see REQ-004). The computational feasibility and accuracy is to be verified seperately.  

________________________

**REQ-0014 - Mass**   

*The maximum mass of the GMA shall be equal or below 5 kg with a measurement accuracy of +/-0.1 %.*  

Verification method(s):  

- **A**: Prior to release of manufacturing drawings, the mass is to be estimated in the CAD-environment. 

- **I**: The mass of the entire GMA shall be measured with an appropriate scale. Divergent measurement accuracies shall be documented.  

________________________

**REQ-013 - Geometrical envelope**  

*A damage- and collision-free motion under worst case angle conditions is required between the Igniter´s main body (incl. it´s attachments) and the GMA geometry. A minimum clearance of 20 mm is to be considered between moving parts. The maximum geometrical limit of th GMA is given by the mass constraint, the loads and (thermo-)mechanical stress requirements mentioned in this document. The Ignition System´s main body (Ø70 mm) is designed with a vertically offset of 63 mm from the Injection Head (IH) upper flange surface.*  

Verification method(s):  

- **A**: A geometrical analysis in CAD shall prove contact- and collision-free motion with all parts involved (e.g. IH, Igniter body, connectors, sensors etc.).

- **I**: Based on geometrical analysis, a motion investigation between at least IH, GMA and the Ignition System (IGNS) shall be undertaken. The minimum clearance measured is to be documented and pictured.  

________________________  

\clearpage

**REQ-015 - Geometrical interface**  

*For the lower attachment of the GMA, the utilizable surface of the IH features a ring with an inner diameter of Ø100 mm and an outer diameter of Ø170 mm. In total, eight through-holes (Ø9 mm each) are available, spaced at 45° intervals (symetrically along PCD). Eight M8 fasteners are intended to fix the GMA with the IH (minimum tensile ultimate strength per fastener: 800 MPa).*  

Verification method(s):  

- **RoD, I**: The interface constraints are to be extracted from Interface Control Documents (ICD) like [RD03].  

________________________  

## 3.3. Mechanical and thermal requirements  
  
**REQ-016 - Max. payload**  
  
The gimbal will be designed to support a maximum payload mass of 40 kg, corresponding to the Thrust Chamber Assembly (TCA) plus margins of the cryogenic engine.  

________________________  

**REQ-018 - Friction coefficient**  

*To reduce the breaking torque of the actuators, the GMA shall provide a constant friction coefficient equal or lower than 0.1 under mechanical and thermal operating conditions.*  

Verification method(s): 

- **I**: Features of the GMA that allow relative motion (e.g. bearings) shall be subjected to breakaway tests, or similar, to demonstrate a friction coefficient equal to or below 0.1 under at least one loaded condition and at the prevailing ambient temperature (e.g. 20 °C). If cryogenic temperatures cannot be simulated, the fitting configuration of the bearing’s support shall be adjusted to represent cryogenic conditions.

- **T**: Extended tests in terms of mechanical load, cryogenic temperature and duration shall prove that the friction coefficient is constantly kept below the required value and friction phenomena like stick-slip effects are controlled.  

________________________   

**REQ-008 - Plastic Deformation and crack formation**  

*The GMA and its parts shall not undergo plastic deformation, crack formation or other non-recoverable deformation when subjected to the operational conditions defined in this specification. Exceptions can be permissible if non-recoverable deformation is identified as a single, local phenomena, that occurs in extraoRD0inary or single event load case. In this case the non-recoverable deformation is to be justified by analysis at least.*  

Verification method(s):  

- **A**: A linear-elastic mechanical analysis is to be conducted at least, to identify potential plastic deformation. Additonal justificaiton methods like fraction -, Low-Cycle Fatigue analysis (LCF) etc. may be conducted complementary. 

- **T**: Cryogenic rated strain gauges are to be introduced at critical areas to prove plastic deformation or crack propagation under operational testing conditions.  

________________________

**REQ-001 - Operating nominal thrust**  

*The GMA shall transmit a total nominal thrust load of 15 kN.*

Verification method(s): 

- **T**: Common instrumentation like load cells or strain gauges are to be introduced to measure the thrust force of the engine. A less accurate prediction through the actuation force of the TVC-actuators (Thrust Vector Control) can be utilized as long as additional sources of torque and forces are known and validated (bellows stiffness, gimbal friction etc.).  

________________________

**REQ-039 - Quasi-Static Load (QSL)**  

*For single events, the GMA shall sustain an excessive thrust load of 22.5 kN at gimbal angle of 0 °, which includes a safety factor of 1.5 applied to the nominal thrust.*  

Verification method(s):  

see REQ-001 - Operating nominal thrust  

________________________

**REQ-021 - Mechanical and thermal transient**  

*Until steady state conditions are achieved, transient conditions dominate. A cooling from ambient 280 K to 180 K within 10 s is to be considered linearly, with a slope of 10 K/s. This is to be taken into account at the GMA surface, that is connected to the IH upper flange. A chamber overpressure rate of 210 bar/s is to be anticipated for a transinent occasion.*  

Verification method(s):  

- **A**: The pressure ramp-ups and temperature data serve as input data to conduct (thermo-)mechanical analysis for validation.  

- **T**: As soon as the GMA is assembled and prepared for testing, local strain gauges and thermocouples at the GMA may give evidence of transient characteristics.   

________________________

**REQ-020 - Operating temperature**  

*An operating temperature of 120 K to 150 K shall be considered at the IH top flange surface that is connected to the GMA support.*  

Verification method(s):  

see REQ-021 - Mechanical and thermal transient  

________________________  


**REQ-030 - Cycling**  

*The GMA shall sustain a minimum of 1000 cycles, which is derived from preliminary GNC-data.*  

Verification method(s):  

- **A**: LCF analysis is to be performed to justify that the expected lifetime can be sustained by the GMA design.

- **T**: A servo-hydraulic driven test rigs with cooling options shall enable strain-controlled fatigue tests. The test rig is to be sized for max. expected cycles - possibly beyond the expectation mentioned in this specific requirement.  

________________________  

## 3.4. Growth potential requirements  

**REQ-035 - Extended cycling**    

*For further utilization of the GMA for flight qualification and preperation for the moon mission, 26520 cycles are targeted.*  

Verification method(s):  

see REQ-030 - Cycling  

________________________    

**REQ-036 - Lateral misalignment**    

*The GMA shall contain features to compensate lateral misalignment of the thrust vector up to +/-10 mm [RD04].*   

Verification method(s): 

- **RoD**: Design attributes are to be introduced, which shall be part of acknowledged design documents (definition/justification files, manufacturing drawings etc.) to be reviewed prior release. 

- **A**: For a first estimation, thrust misalignment can be computed related to intended tolerances and GD&T prior testing. Worst-case considerations based on manufacturing drawings and quality reports of already manufactured components provide a first reference for a possible thrust vector offset. 

- **T**: Thrust misalignment shall be executed in a loop of hotfire testing accompanied by load cells and/or strain gauge measurements and adapted position of the GMA until the offset of the thrust vector is at its minimium (success criteria TBD).  

________________________ 

**REQ-037 - Vacuum environment**  

*The GMA performance in ambient conditions shall be adapted to operate feasibly in vacuum, especially concerning lubrication, thermal and mechanical loads.* 

Verification method(s):  

- **RoD, A, I, T**: TBD  


\clearpage

# 4. Acronym List  
The acronyms used in this document are listed below.  

| **Acronym**  | **Definition**   |
|---|---|
|GMA|Gimbal Mount Assembly|
|ICD|Interface Control Document|
|IGNS|Ignition System|
|IH|Injection Head|
|LCF|Low-Cycle Fatigue|
|TEC|The Exploration Company|
|TVC|Thrust Vector Control|