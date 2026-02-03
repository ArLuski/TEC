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
status of the development associated to the requirement consolidation [RD1]. The main objective is to demonstrate that the product meets the specified requirements considering the resources, capabilities, costs and schedule of this project.

## Compliance Statuses  
The following compliance statuses are used:

- **C** (Compliant): the requirement is considered applicable and is implemented in the design

- **NA** (Not Applicable): the requirement is considered not applicable to the system (e.g. berthing-related requirements are not applicable to a docking vehicle.)

- **T** (Tailored): the requirement is not fulfilled to its full extent. The compliance comment will indicate the limitations.

- **NC** (Not Compliant): the requirement, although considered applicable, is not taken into account in the design.


## Reference
[RD1] Gimbal Mount Assembly Requirement Consolidation - Version 0

[RD2] Space engineering - Verification - ECSS-E-ST-10-02C Rev.1 01.02.2018

[RD3] Huracan - TCA Interface Control Document - TEC-FRA-DOC-202401143 - Version 1-draft

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
The verification methods used for the development of the GMA are closely aligned with The Exploration Company’s (TEC) verification policy and the ECSS standard [RD2]: *Review of Design, Analysis, Inspection, and Test*. Verification shall be carried out using one or more of these methods.

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

# Preliminary Verification Control Document  

## Environmental requirements  

**REQ-00X - Pollution requirements** 
*Sensitive areas, such as regions of relative motion, shall be protected against sand particles with an average size of 0.2 mm at a temperature of 49.6 °C.*  

Verification method(s):  
- **I**: The absolute temperature of the sand heap located near the vehicle launch area shall be measured prior to launch using a calibrated digital temperature sensor (e.g., soil thermometer).

Particle size distribution shall be assessed by measuring ten randomly selected sand particles using a caliper.

The investigation shall be accompanied by appropriate documentation of ambient environmental conditions, including air temperature, relative humidity, atmospheric pressure, and wind speed.  
________________________

**REQ-00X - Ambient requirements**  
*According to the system requirements of *Oneiros*, the sea level conditions are defined by an pressure of 0.994 bar to 1.0276 bar and 12 % to 91 % humidity. The ambient temperature ranges from 8.3 °C to 49.6 °C.*
 
Verification method(s): 

- **I / T**: The absolute ambient temperature is to be measured with simple instrumentation like a thermometer (RTDs) or thermistor. 

The environmental pressure can be measured by a barometer (mechanical or electronic pressure sensor).

A hygrometer measures relative humidity. Digital sensors (capacitive or resistive) are common.

All values are to be referenced and documented w.r.t the local meteorological station´s measurements.  
________________________

## 2.2. Functional requirements  

**REQ-003 - Operational gimbal capability**  

*The GMA design provides a deflection capability of ±10° per axis (pitch and yaw), which covers the GNC needs as well as the mechanical limits of the subsystem and its components (e.g., bellows and actuators).*  

Verification method(s): 

- **A**: A kinematic analysis in CAD shall prove the gimbal capability on a component and system level of the entire engine, including ducts, actuators etc.

- **I**: Prior to assembly of the GMA it´s deflection angles are to be measured. From the neutral position (gimbal angle 0 °), the deflection up to +/-10 ° is to be determined, e.g. by prior markings between surfaces that are subjected to relative motion.  
________________________

**REQ-00X - Max. gimbal capability**  

*For off-nominal cases and emergency authority, the max. gimbal angle shall not exceed +/-12 °.*  

Verification method(s):  

see REQ-003 - Operational gimbal capability 
________________________

**REQ-002 - Rotation axis**  

*To provide full pitch and yaw control capability, a two-axis rotation mechanism shall be implemented. Both axes are positioned perpendicular to each other within the same horizontal plane.*  

Verification method(s):  

- **RoD**: The manufacutirng drawing shall contain dimensions and tolerances related to the horizontal plane of both axis and the perpendicularity. 

- **A / RoD**: Analysis of tolerances based on manufacturing drawings and quality reports can be utilized for post-machined investigations of the axis´ perpendicularity. This needs to be executed with the GMA fully assembled in order to account for the bearings’ degrees of freedom, clearances, etc.

- **I**: For inspection, the measurement of the perpendicularity of both axis can be done by reference planes with simple gauges like a precision square under ambient and unloaded conditions. This is to be realized for the entire angle range of the gimbal.  
________________________  

**REQ-004 - Angular velocity**  

*To compromise GNC needs with mechanical constraints of the engine such as the actuator capacity, the max. angular velocity of the engine is 20 °/s.*  

Verification method(s):  

- **A**: A kinematic analysis is to be executed to determine the angular velocity based on the linear velocity of the actuators. 

- **T**: The angular velocity can be computed by speed sensors measurements. A proper instrumentation is to be chosen to account for operational constraints (e.g. temperature, vibration).  
________________________

**REQ-005 - Angular acceleration**  

*The engine´s acceleration and hence, the capability of the GMA shall be max. 25 rad/s².*  

Verification method(s):  

- **A**: A kinematic analysis is to be executed to determine the angular acceleration based on the linear acceleration of the actuators. 

- **T**: The angular acceleration can be derived mathematically by signal processing from angular velocity measurements (see REQ-004). The computational feasibility and accuracy is to be validated seperately. 
________________________

**REQ-0014 - Mass**   

*The maximum mass of the GMA shall be equal or below 5 kg with a measurement accuracy of +/-0.1 %.*  

Verification method(s):  

- **A**: Prior to release of manufacturing drawings, the mass is to be estimated in the CAD-environment. 

- **I**: The mass of the entire GMA is to be measured with an available scale. Divergent measurement accuracies are to be documented. 
________________________

**REQ-00X - Geometrical envelope**  

*A damage- and collision-free motion under worst case angle conditions is required between the Igniter´s main body (incl. it´s attachments) and the GMA geometry. A minimum clearance of 20 mm is to be considered between moving parts. The maximum geometrical limit of th GMA is given by the mass constraint, the loads and (thermo-)mechanical stress requirements mentioned in this document. The Ignition System´s main body (Ø70 mm) is designed with a vertically offset by 60 mm from the Injection Head (IH) upper flange surface.*  

Verification method(s):  

- **A**: A geometrical analysis in CAD shall prove contact- and collision-free motion with all parts involved (e.g. IH, Igniter body, connectors, sensors etc.).

- **I**: Based on geometrical analysis, a motion investigation between at least IH, GMA and the Ignition System (IGNS) is to be undertaken. The minimum clearance measured by a ruler is to be documented and pictured.  
________________________  

**REQ-015 - Geometrical interface**  

*For the lower attachment of the GMA, the usable surface of the IH features a ring with an inner diameter of Ø100 mm and an outer diameter of Ø170 mm. In total, eight through-holes (Ø9 mm each) are available, spaced at 45° intervals (symetrically along PCD), to fasten the GMA to the IH using eight M8 fasteners (minimum tensile ultimate strength per fastener: 800 MPa).*  

Verification method(s):  

- **RoD, I**: The interface constraints can be extracted from the Interface Control Document (ICD) [RD3] and executed inspections (if already conducted). Same needs to be done w.r.t. to the upper flange interface that connects the GMA with the thrust frame.   
________________________  

## 2.3. Mechanical and thermal requirements  

**REQ-018 - Friction coefficient**  

*To reduce the breaking torque of the actuators, the GMA shall provide a constant friction coefficient equal or lower than 0.1 under mechanical and thermal operating conditions.*  

Verification method(s): 

- **I**: Features of the GMA that allow relative motion (e.g. bearings) shall be subjected to breakaway tests or similar to prove a friction coefficient equal or below 0.1 in a at least loaded condition and the prevailing ambient temperature (e.g. 20 °C). If cryogenic temperatures can´t be simulated, the fitting configuration of the inner- and outer ring of the bearing is to be adjusted as if cryogenic temperature is present. 

- **T**: Extended tests in terms of mechanical load, cryogenic temperature and duration shall prove that the friction coefficient is constantly kept below the required value and friction phenomena like stick-slip-effects are controlled. 
  
________________________  

**REQ-008 - Plastic Deformation and crack formation**  

*The GMA and its parts shall not undergo plastic deformation, crack formation or other non-recoverable deformation when subjected to the operational conditions defined in this specification. Exceptions can be permissible if non-recoverable deformation is identified as a single, local phenomena, that occurs in extraordinary or single event load case. In this case the non-recoverable deformation is to be justified by analysis at least.*  

Verification method(s):  

- **A**: A linear-elastic mechanical analysis is to be conducted, to identify potential plastic deformation. Additonal justificaiton methods like fraction mecchanical, Low-Cycle Fatigue analysis (LCF) etc. may be conducted complementary. 

- **T**: Cryogenic rated strain gauges are to be introduced at critical areas to prove plastic deformation or crack propagation under operational testing conditions.

________________________

**REQ-001 - Operating nominal thrust**  

*The GMA shall transmit a total nominal thrust load of 15 kN.*

Verification method(s): 

- **T**: Common instrumentation like load cells or strain gauges are to be introduced to measure the thrust force of the engine. A less accurate prediction through the actuation force of the TVC-actuators (Thrust Vector Control) can be utilized as long as additional sources of torque and forces are validated (bellows stiffness, gimbal friction etc.). 

________________________

**REQ-00x - Quasi-Static Load (QSL)**  

*For single events, the GMA shall sustain an excessive thrust load of 22.5 kN at gimbal angle of 0 °, which includes a safety factor of 1.5 applied to the nominal thrust.*  

Verification method(s):  

see REQ-001 - Operating nominal thrust
________________________

**REQ-00x - Mechanical and thermal transient**  

*Until steady state conditions are achieved, transient conditions dominate. A cooling from ambient 280 K to 180 K within 10 s is to be considered linearly, with a slope of 10 K/s. This is to be taken into account at the GMA surface, that is connected to the IH upper flange. A chamber overpressure of 210 bar/s is to be anticipated for a transinent occasion.*  

Verification method(s):  

- **A**: The pressure ramp-ups and temperature data serve as input data to conduct (thermo-)mechanical analysis for validation.  

- **T**: As long as the GMA is assembled and prepared for testing, local strain gauges and thermocouples at the GMA may give evidence of transient characteristic  

________________________

**REQ-020 - Operating temperature**  

*An operating temperature of 120 K to 150 K shall be considered at the IH top flange surface that is connected to the GMA support.*  

Verification method(s):  

see REQ-00x - Mechanical and thermal transient

________________________  


**REQ-030 - Cycling**  

*The GMA shall sustain a minimum of 1000 cycles, which is derived from preliminary GNC-data.*  

Verification method(s):  

- **A**: LCF analysis is to be performed to justify that the expected lifetime can be sustained by the GMA design.

- **T**: Servo-hydraulic driven test rigs with cooling options shall enable strain-controlled fatigue tests. The test rig is to be sized for max. expected cycles beyond the expectation mentioned in this requirement.

________________________  

## 2.4. Growth potential requirements  

**REQ-00x - Extended cycling**    

*For further utilization of the GMA for flight qualification and preperation for the moon mission, 26520 cycles are targeted.*  

Verification method(s):  

see REQ-030 - Cycling  

________________________    

**REQ-00x - Lateral misalignment**    

*The GMA shall contain features to compensate lateral misalignment of the thrust vector up to +/-10 mm [RD4].*   

Verification method(s): 

- **RoD**: Design attributes are to be introduced in the GMA to correct thrust misalignment, which shall be part of acknowledged design documents (definition/justification files, manufacturing drawings etc.)  

- **A**: Thrust misalnignment can be computed prior testing. Worst-case considerations based on manufacturing drawings and quality reports of already manufactured components provide a first reference for a possible thrust vector offset. 

- **T**: Thrust misalignment shall be executed in a loop of hotfire testing accompanied by load cells or strain gauge measurements and adapted position of the GMA until the offset of the thrust vector is at its minimium


________________________  

**REQ-00x - Vacuum environment**  

*The GMA performance in ambient conditions shall be adapted to operate feasibly in vacuum, especially concerning lubrication, thermal and mechanical loads.* 

Verification method(s):  

TBD

\clearpage

# Acronym List  
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