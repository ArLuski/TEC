<!--- First page -->

---

---
<div style="page-break-after: always;"></div>


## 1 Introduction
### 1.1 Scope
Based on preliminary requirements initially shared by TEC for this activity [RD1], this document refines the key performance parameters. These updated requirements are primarily associated to the Hopper Ground Demonstrator "Oneiros", which is also part of a de-risking activity of the "Huracan" propulsive system [RD2]. Since the engine design will be close to the flight configuration of the Lunar Mission "Hilal", the current constraints and intentions of the "Huracan" engine are taken into account for future utilization of the GMA. This is mainly covered under the chapter 1.3.4 and applies only if hard requirements (functional, mechanical, thermal, environmental) are met and business related constraints (budget, delivery time etc.) remain unchanged. 

### 1.2 Reference

[RD1] Consultant Agreement 12.12.2025- Docusign Envelope ID:  AA5722EA-0E20-45A6-BFE2-2B6D313A7FF3

[RD2] TEC-ITA-DOC-2025-01011 - Version 3 - Design Description and Justification File 

[RD3] TEC-ITA-DOC-2025-01017 - Version 0 - System Requirements Document

[RD4] Modern Engineering for design of liquid propelleant rocket engines - D.Huzel / D.Huang, Vol. 147, p. 341


## 1.3 Requirements
### 1.3.1 Functional requirements

**REQ-003 - Operational gimbal capability**  
The GMA design provides a deflection capability of +/-10° per axis (pitch and yaw) to serve intended GNC manfouvers during operational flight conditions.

**REQ-00X - Max. gimbal capability**  
For off-nominal cases, emergency authority of the design, the max. gimbal deflection shall not exceed +/-12°. 

**REQ-002 - Rotation axis**  
To provide full pitch and yaw control capability, a two-axis rotation shall be provided. Both axis are located perpendicular (90°) with respect to each other in the same horizontal plane. 

**REQ-004 - Angular velocity**   
To compromise GNC needs with mechanical constraints of the engine such as the actuator capacity, the max. angular velocity of the engine is 20°/s. 

**REQ-005 - Angular acceleration**  
The engine´s acceleration and hence, the capability of the GMA shall be max. 25 rad/s².

**REQ-0014 - Mass**   
The maximum mass of the GMA shall be equal or below 5kg with an mass measurement accuracy of +/-0,1%.

**REQ-00X - Geometrical envelope**  
A damage- and collision-free motion under worst case angle conditions is required between the Igniter´s main body (incl. it´s attachments) and the GMA geometry. A minimum clearance of 20 mm is to be considered between moving parts. The maximum geometrical limit of th GMA is given by the mass constraint, the loads and (thermo-)mechanical stress requirements mentioned in this document. The Ignition System´s main body (Ø70 mm) is designed with a vertically offset by 60 mm from the IH upper flange surface. 

**REQ-015 - Geometrical interface**   
For the lower attachment of the GMA, the utilizable surface of the IH features a ring with an inner/outer diameter of Ø100mm/Ø170 mm. In total, 8x45°-Ø9mm through holes are available to fasten the GMA with the IH by 8xM8 fasteners (min. tensile strength per fastener 800 MPa). The fasteners are symmetrically distributed on the PCD.

### 1.3.2 Mechanical and Thermal requirements

**REQ-018 - Friction coefficient**  
To reduce the breaking torque of the actuators, the GMA shall provide a friction coefficient equal/lower than 0.1 under sea level conditions, a total nominal thrust of 15 kN and thermal steady state condition of 160K at the gimbal attachment surface at the IH flange. 

**REQ-008 - Plastic Deformation and crack formation**  
The GMA and its parts will not undergo plastic deformation, crack formation or other non-recoverable deformation when subjected to the operational conditions defined in this specification. Exceptions can be permissible if non-recoverable deformation is identified as a single, local phenomena, which can can justified by analysis. 

**REQ-001 - Nominal thrust**  
The GMA shall transmit a total nominal thrust load of 15 kN.

**REQ-00x - (Quasi-)static thrust level**   
For single events the GMA shall sustain an escessive load of 22.5 kN, which includes a safety factor of 1.5 applied to the nominal thrust.

**REQ-030 - Cycling** 
The GMA shall sustain a minimum of 1000 cycles, which is derived from preliminary GNC-data. 

**REQ-020 - Operating temperature** 
The nominal operating temperature at the GMA surface that is connected to the IH flange lies at 150K +/-10K. 

**REQ-021 - Thermal transient** 
Until steady state conditions are achieved, transient conditions dominate. A cooling from ambient 280 K to 180 K within 10 s is to be considered in a linear relation ship with a slope of 10 K/s. This is to be taken into account at the GMA surface, that is connected to the IH. 

### 1.3.3 Environmental requirements

**REQ-00X - Polution requirements**  
Protection of sensitive areas (e.g. areas of relative motion) by sand particles of an average size of 0.2mm at a temperature of 49.6°C [RD3]

**REQ-00X - Ambient requirements**  
Following the system requirements of Oneiros, the sea level conditions are defined by an pressure of 0.994 bar to 1.0276 bar and 12% to 91% humidity. The ambient temperature ranges from 8.3°C to 49.6°C. [RD3]

### 1.3.4 Growth potential requirements

**REQ-00x - Cycles**  
For further utilization of the GMA for flight qualification and preperation for the moon mission, a value of 26520 cycles are targeted as long as no inspection intervals are intended. 

**REQ-00x - Geometrical envelope**  
The GMA design shall be flexible to adapt different kind of geometrical conditions. Future design intentions, where the Ignition System is meant to be printed in one compact part with the IH is to be considered. 

**REQ-00x - Lateral misalignment**  
To reduce demands to vehicle´s guidance and the engine-actuation system, the thrust vector must be prealigned in all three axis. Hence, the GMA shall contain features to compensate lateral misalignment up to +/-10 mm. [RD4]

## 5 Acronym List

| Acronym  | Definition   |
|---|---|
|IH|Injection Head flange|
|GMA|Gimbal Mount Assembly|
|PCD|Pitch Circle diameter|
|QSL|Quasi-static load|
|TEC| The Exploration Company|
