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
It contains the overall Manufacturing, AIT activities, suggestions for associated verification tools (GSE - Ground Support Equipment) and the involved documentation.

## 1.2. Reference  

[RD1] Gimbal Mount Assembly - Definition File / Version 001  

[RD2] Gimbal Mount Assembly - Interface Control Document / Version 001  

[RD3] Data Sheet - ARMCO 17-4PH / 2022  

[RD4] Instructions for Double Anvil Spherical Bearing Swaging Tool #10 Wide / Pegasus Auto Racing Supplies, Inc.  

[RD5] Bearing Installation and Retention by Swaging or Staking / AIA - NAS0331 / 2013  

[RD6] NASA Reference Publication 1228 - Fastener Design Manual / Richard T.Barrett / 1990  

[RD7] Nyx Moon - Huracan Development Logic / TEC-FRA-DOC-2024-01004 / Issue 02  

[RD8] Gimbal Mount Assembly - Justification File/ Version 001  

[RD9] Structural Design and TEst Factors of Safety For Spaceflight Hardware / NASA-STD-5001B / Change 3 /

[RD10] Gimbal Mount Assembly - Preliminary Verification Control Document / Version 001  

[RD11] Nyx Moon - Huracan Overall Test Plan / TEC-FRA-DOC-2024-01005/ Issue 01  



\clearpage
 

# 2. GMA Presentation  

As the primary thrust-transmitting interface, the Gimbal Mount Assembly (GMA) connects the engine to the vehicle, transfers engine thrust to the vehicle structure, and allows the engine to gimbal relative to the vehicle structure for thrust-vector control. The design is detailed in the Definition File [RD1] and the Interface Control Document [RD2].

![GMA isometric view](../WP3/figures/GMA_isometric.png){width=30%}

# 3. Manufacturing  

The manufacturing process shall follow the companies established and proven internal processes from sourcing of the raw material until final manufacturing and subsequent quality related processes. The following figure shows the parts that shall be custom machined, while the rest are of COTS-nature as described in [RD1]. 

![Custom machined parts of the TMA](../WP3/figures/GMA_explosion_custom.png){width=50%}

## 3.1. Materials and Heat Treatment

All custom machined parts of the GMA (Figure 2) are made of martensitic precipitation hardened stainless steel, that combines high strength, excellent corrosion resistance, easy heat treatment and comparable thermal expansion w.r.t Inconel 718 (engine). As one of the main structural parts of the engine, the GMA is treated as a critical application. For this, the material shall be sourced in a precipitation hardned condition. The final material choice is **17-4PH - H900**, while the suffix expresses the heat treatment condition. The figure below shows a general overview of material properties as a function of the precipitation hardened conditions ranging from *H900* to *H1150M*.

![17-4PH, Typical Mechanical Properties - Bar](<../WP3/figures/17-4PH properties.png>){width=80%}  

In case of sourcing issues of the chosen heat treament condition *H900*, the alterantive condition *H1025* can be taken for all parts consistently.  

## 3.2. Machining 

The GMA Lug Head and Clevis Head are recommended to be manufactured using a 5-axis CNC machine to achieve the required precision and produce the complex geometries specified in the manufacturing drawings.  

The Spacer and Bushing shown in Figure 2 may be manufactured by precision turning, as these components determine the radial clearance and the axial positioning accuracy of the adjacent parts.

The final manufacturing strategy shall be determined by the manufacturer, provided that all requirements specified in the manufacturing drawings are met.

# 4. Assembly  

This chapter describes the required tools and procedures to assemble the GMA. 

## 4.1. Required Tools  

The tools required mount the GMA are listed below:

- Hydraulic press to position the Spherical Bearing *MS14103-10* with the GMA Lug Head with a required force of 21.375 lbs +/- 3,000 (95kN +/-13kN) [RD4]
- Double Anvil Spherical bearing Swaging Tool for Spherical Bearing *MS14103-10* in accordance aligned to [RD5]
- Troque Wrench for Bolt NAS6710D29 and Nut MS9358-016
- Torque Wrench for ISO4017-M6x16/25-A4-70 hexagon head screws and ISO4032-M6-A4-70 hexagon regular nuts
- Pliers to bend the Cotter Pin in place

## 4.2. Assembly Sequence  

The sequence of the assembly is described in this chapter. The subsequent description shall be accompanied during practical execution along side dedicated 3D data (CAD-ID: 126703/01). 

The assembly is divided in two main steps (Figure 4).  

![GMA - Assembly steps](<../WP3/figures/GMA_assembly steps.png>){width=100%}  

In the **first step** (Figure 4, left), the Spherical Bearing *MS14103-10* is inserted into the Clevis Lug Head. Due to the interference fit  between the Inner Race of the Spherical Bearing and the Lug Head from *-0.0055 mm to +0.0202 mm*, a mounting force will be required. Lubricant on the outer race of the bearing is recommended to be applied (e.g. Ethanol, Loctite 609) to prevent lock-up or galling. This force shall be centrically introduced by a hydraulic press through a customized Anvil (CAD-ID: 2020/01). The purpose of this customized GSE tool is to position the bearing so that it´s width is aligned with the width of the GMA Lug Head. In addition, the tool allows the mounting force to be transmitted through the outer race of the Spherical Bearing only and thus protect the PTFE-fabric liner from being damaged or worn prior engine operation. The anvil swaging of the bearing over housing is then executed following *Method 100* [RD5]. Detailed instruction details are to be extracted from the manual [RD4] or in chapter 7.1 and complementarily in [RD5].

The **second step** (Figure 4, right) shows the sequence of the remaining part to the full assembly. While the GMA Lug Head and the Spherical Bearing is united through swaging as mentioned above and detailed in [RD4] and [RD5], this subassembly is then connected to the GMA Clevis Head. The remaining parts exhibit a clearance fit, so that no specific precautions and preparations are needed to make the assembly (and later disassembly) possible under ambient temperature. Following the numbering sequence in the image from two to eight, the Spacer (2) and the GMA Lug Head subassembly (3) are coaxially centered within the GMA Clevis Head holes (8). It is important to note, that the GMA Clevis Head Ears are designed asymmetrically for functional reasons. Hence,  the Spacer (2) is positionied at the Clevis inner side between the smallest bore of the Clevis and the Inner Race of the Lug-subassembly. The Bushing (4) is then axially inserted through the bigger bore from outside on the opposite side of the Clevis until it is axially in contact with the inner race of the Spherical Bearing. Once the Spacer (2), the Lug-subassembly (3) and the Bushing (4) are positioned in place, the Bolt *NAS67103D29* (5) is pushed through from the side where the Bushing is located up to the oppposite side of the Clevis Head (8). The Bolt *NAS67103D29* (5) is then tighted by hand with the Castellated Nut *MS9358-016* (6) on the opposite, outer side of the GMA Clevis Head (8). After a hand-tight preload between the Bolt and Nut, the Nut´s preload is then increased until the next slot of the nut aligns with the drilled hole of the bolt. This final applied torque is to be controlled and documented. After appliction of the torque, both parts shall be secured from loosening with the Cotter Pin *MS24665-374*. In accordane to NASA recommendations [RD6], the Cotter Pin shall be bended with pliers as illustrated in Figure 5.  

![Bending of Cotter Pin [RD6]](<../WP3/figures/GMA_NASA_thread locking.png>){width=30%}   

# 5. Integration  

After the GMA is assembled to a component, it will be integrated to the engine system on one side and the vehicle on the other.

As elaborated in the Definition File [RD1], the GMA is not directly attached to the engine or vehicle. The engine is rather interfaced by a Thrust Dome on the engine side and four Thrust Frame Beams on the vehicle side. 

**GMA-Engine**  
Eight hexagonal head screw fasteners and two Ø 4m6 Dowel Pins are provided to connect the GMA with the engine (Figure 6). The GMA is interfaced with the engine by the Thrust Dome [RD1]. The positioning of the Dowel pins are designed for a tighter fit on the Thrust Dome side. Thus, the pins shall be inserted on the Thrust Dome flange first. Thereafter the GMA Lug Head is centered on the Thrust Dome through the Dowel Pins, followed by preloading all eight M6 fasteners in a criss-crossed ("star") pattern. For a proper execution, the tightening is done in multiple steps, so that all bolts are hand tighten first, then tighten to 30 % of the target torque, followed by 60 % and finally 100 % of the torque listed in the Table 1.  

![Interface assembly - GMA Lug Head and Thrust Dome](<../WP3/figures/ICD_GMA Thrust Dome2.png>){width=65%}  

**GMA-Vehicle**  
As indicated in the Interface Control Document [RD2], 16 fasteners (bolts, washers, nuts) are provided to fix the GMA Clevis Head with the Thrust Frame beams. Figure 7 below shows the configuration and orientation of the fasteners. 

![Interface assembly - GMA Clevis Head and Thrust Frame Beams](<../WP3/figures/GMA_vehicle interface.png>){width=80%}  

Before applying torque, all beams shall be appropriatly positioned and centered by four centering features as shown in Figure 4 in [RD2]. Since the bolt pattern between the Thrust Beam Structure and GMA Clevis Head is different from standard flange configurations (all bolts in one plane), the torque sequencing of the fasteners might be adapted in further design iteration. In order to provide a homogenous bolt pretention over the entire flange, the preload sequence is recommended to follow the criss-crossed tightening of the vertical fasteners  first (x-axis) and then followed by horizontal fasteners in the second step (yz-plane). All four Thrust Frame Beams shall be tightened progressively, not one beam completely before moving to the next. After application of a light seating preload (hand tight) to every single beam, the beams are then preloaded opposite in a criss-crossed pattern as recommended for the GMA Lug Head above in 30 %, 60 % and 100 % of the preload presented in Tablle 1. Hence, after hand tightening of all fasteners, the preload application shall be sequenced in accordance to the numbering presented in Figure 8 . The image shows a bottom view towards the Thrust Beam Structures in the yz-plane, while the GMA Clevis Head is hidden. The Thrust Vector *F_thrust* (green) points into the image plane, just like all blue colored fasteners for reference. All red colored fasteners are oriented in the yz-plane (perpendicular to *F_thrust* and blue colored fasteners).

![Numbering for preload sequence between GMA Clevis Head and Thrust Frame Beams](<../WP3/figures/GMA_vehicle bolt pattern.png>){width=80%}  

| **Interface**| **Thread type** | **Designation** |**Preload (Nm)** | 
| ------ | ----- | ----- | ----- | 
| GMA Lug Head - Thrust Dome          |Through-Thread  | ISO4017-M6x16-A4-70  | ??? |
| GMA Clevis Head - Thrust Frame Beam |Through-Thread  | ISO4017-M6x16-A4-70  | ??? |
| GMA Clevis Head - Thrust Frame Beam |Bolt-Nut        | ISO4017-M6x25-A4-70  | ??? |
: Preload of fasteners for integration  

# 6. Test 

The GMA is subjected to a verification programme appropriate to their development status and intended use. In accordance with common ECSS and NASA terminology, the tests are grouped into three main categories:
  
- **Acceptance Tests**
- **Development Tests**
- **Qualification Tests**

The following chapters describe the objectives, scope, methods, and acceptance criteria for each test category.

## 6.1. Testing Strategy  

1. Preliminary Development Phase: Acceptance tests on part-level and early testing for risk reduction shall take place during the dedicated TVC test campaign *H05*. 

2. Development Phase: Detailed design phase using an iterative approach alongside testing of the Development Models. A total of four Development Models are tested as part of test campaigns: DM1 to DM4 [RD7]. Important to note is that the DM1-campaign already took place beginning 2026 without the GMA, but a rigid Thrust Structure. After passing the Derisking Phase, the GMA shall enter the Development Phase earliest in DM2.
   
3. Qualification Phase: Testing begins at the Final Design Key Point and continues up to the Ready for Flight
review to ensure the Huracan engine’s readiness for its first mission

## 6.2. Acceptance Test  

Acceptance Tests are performed on each manufactured part to verify conformity, workmanship, structural integrity, and basic functionality before assembly to a component and higher-level engine system testing later. After successful GMA component acceptance tests, the hardware proceeds to a subsystem testing in the *H05* campaign, which also encompasses the TVC-actuators and the bellows with representative routed and pressurized ducts. This campaign is understood as part of acceptance that is required for early derisking and entry of engine-level testing in the frame of Development Tests. 

### 6.2.1. Inspection  

Each GMA part will be inspected prior entering the acceptance tests. It consists of a visual inspection using
a microscope if required, as well as the measurement of main physical properties such as mass and main
dimensions. Material certificate and heat treatment checks, such as GD&T inspection according to specifications in manufacturing drawings are also reviewed during the incoming inspection. Among the custom machined parts, the main dimensions of the assembled COTS parts are to be inspected and documented in accordance with the standards specifications. 

Inspection also relates to an assembled inspection, particularily when the Spherical Bearing is swaged with the GMA Lug Head (see chapter 4.2). Inspection related aspects are to be extracted in the procedures and quality assurance provisions for Method 100 in [RD5].

**Sucess criteria**  

• Surface:  
No cracks, scratches, dents, deviations of surface finishes (see manufacturing drawings) or signs of corrosion that may affect the part’s structural integrity. 

• Cleanliness:  
The parts are free from contaminants like dirt, grease, debris or chips.  

• Material anomalies:  
Check for any visible signs of material inconsistency, such as discoloration, uneven texture,
porosities. Check also for conformity of material certificate, heat treatment and thermal/mechanical properties in accordance with assumptions during theoretical analysis.

• Accuracy of Dimensions and Tolerances:  
Critical dimensions and tolerances (GD&T) match design specifications, ensuring that the part is within its specification.  

• Collision:  
Review of geometrical contact during max. displacement between moving parts in an assembled configuration  

• Friction:  
Friction of Bearing particularily in accordance with the standard requirements

• Tooling:  
Given assurance of appropriate usage of tooling is essential. This is especially important for the Double Anvil Spherical bearing Swaging Tool [RD55]

### 6.2.2. Proof Tests  

Per NASA definition [RD9] a Proof Test shall screen defects in workmannship, material quality to verify structural integrity. Given the timeline related constraints of the project and the lacking availibility of internal testing resources, the GMA shall not be proof tested through application of a representative load (e.g. quasi-static load). Considering the conservative load assumptions during the theoretical analysis in [RD8], the load capabilities of the military-rated COTS parts (Bolt, Nut, Bearing) and the chosen material, no testing shall be executed to verify load-related verification requirements listes in [RD10]. Here, the verification by analysis only shall be sufficient to proceed to further testing. Additionally, any simplified load application other then the one tested on a Development Model (engine level), will not be representative to give evidence for a successfull Acceptance Test. This is mainly driven by the nonlinear behaviour of the bearings PTFE-fabric liner and its load-dependend change of friction coefficient. 

Unlike described in [RD5], the Spherical Bearing *MS14103-10* shall not be proof tested for push out of the bearing. Instead, after the staking process, the bearing groove shall be gauged as stated in [RD4] or respectively shown chatper 7.1. A push out test is not desired as long as the staking process is consistently followed in alignment to the recommendations in [RD4]. It is also assumed that the press fit between the outer ring of the bearing and the GMA mounting head ensures correct positioning.

**Sucess criteria**  

Sucess criteria are not defined as Proof Tests will not be executed.

### 6.2.3. Functional Tests  

**Roll Error**  
The engine’s ability to limit roll motion of the vehicle, corresponding to rotation about the x-axis, is determined by the minimum geometric clearance between the Anti-Roll Features of the GMA Lug Head and the inner surfaces of the GMA Clevis Head.

The clearance shall be measured at all four relevant locations. The smallest measured clearance governs the maximum permissible roll angle.

When the Lug Head is perfectly centred within the Clevis Head, the clearance is nominally 0.3 mm at each of the four locations. This corresponds to a roll error of less than 0.8 °.

![Gauging of Roll-Error](<../WP3/figures/GMA_roll gauging.png>)(width=80%) 

**Gimbal angle**  
The gimbal angle of the GMA Lug Head about the z-axis (yaw) is limited by a mechanical stop to a nominal value of ±12° [RD1]. The gimbal angle about the y-axis is limited by the available stroke of the TVC actuators.  

The maximum gimbal angle about the z-axis is particularly important because the mechanical stop prevents the spherical bearing from exceeding its maximum permissible oscillation angle of ±12 °.  

The maximum gimbal angle can be verified using a magnetic digital angle gauge with a resolution of up to 0.1°. For the measurement, the fixed GMA Clevis Head shall be securely positioned, and the GMA Lug Head shall be vertically aligned in its neutral position, corresponding to an angle of 0°.  

The Lug Head shall then be displaced relative to the fixed Clevis Head in a controlled and precise manner until the mechanical stop is reached in both directions +12 ° and -12 °. Measurement accuracy and repeatability can be improved by minimizing any unintended roll motion during displacement.  

**Geometrical Collision**  
During oscillation of the GMA Lug Head, it shall be visually verified that contact between the GMA Lug Head and the GMA Clevis Head occurs only at the intended contact locations.

During displacement toward the maximum roll angle, contact shall occur between the anti-roll features of the GMA Lug Head and the corresponding inner surfaces of the GMA Clevis Head.

As specified in [RD1], when the maximum yaw angle is reached, the designated mechanical stops within the GMA Clevis Head shall be the first features to come into contact. Prior contact between the Clevis Head and the bolt, or with any other component or surface having limited clearance, is not permissible. Potential areas, where attention needs to be payed are shown exemplarily in the **Figure ???**.

![GMA - Potential for geometrical Collision](../WP3/figures/GMA_yaw12deg_collision.png)  

**Breakaway Torque**  
The breakaway torque of the spherical bearing MS14103-10 is the torque required to initiate relative angular movement between the inner and outer races when the inner race is held stationary and no external load is applied.  

Verification of the breakaway torque is important for demonstrating TVC functionality and shall be completed as part of the acceptance testing no later than the completion of H05.  

Two separate measurements shall be performed to evaluate any change in bearing friction:

- Bearing-only condition:
  The breakaway torque of the uninstalled bearing shall be measured in accordance with the applicable requirements of MS14103.

- Installed and swaged condition:
The breakaway torque shall be measured after the bearing has been installed and swaged into the GMA Lug Head. This measurement shall account for any influence of the installation process and the interference fit on bearing friction.
   
**Sucess criteria**  

| **Functional feature**| **Sucess criteria** | **Comment** | 
| ------ | ----- |----- |
| Roll Error |max. 0.3 mm| equals angle error of 0.8 °|
| Gimbal angle |max. 12 °| Overshooting limits bearing lifetime|
| Geometrical Collision |Controlled contact| Contact with intended surfaces first|
| Break Away Torque bearing only |max. 8 IN-LB | Equals 0.9 Nm|
| Break Away Torque bearing swaged |< 8 IN-LB | Bearing friction decreases with pressure|
: Sucess criteria for functional GMA tests 

## 6.3. Development Test  

Development tests are conducted during the design-maturation phase to build confidence in new designs and concepts aligned with the Overall Test Plan objectives on the engine system level in alignment to [RD11].  

Development-test conditions can extend beyond the normal design or operating range where this is necessary to identify credible weaknesses or design deficiencies. Development testing is iterative and can be performed concurrently with design modifications. However, successful development testing does not, by itself, constitute qualification unless the test article, configuration, test levels, durations, instrumentation, procedures, and success criteria satisfy all applicable qualification requirements.  

The current GMA represents the first design iteration within the project. During the development of the design, it could be shown, that parallel developments of adjacent components have an immediate and meaningful impact on the GMA design and its representativity for future development and qualification models. As shown in the Justification File [RD7] for instance, the GMA is not designed for thermal loads. This is given by the current design of the Thrust Dome that is a dependend of the Ignition System design (IGS) update and the mission duration of the on-Earth demonstrator *Oneiros* of less then *60s*. When the IGS design changes in favor of more compactness and mass reduction (as desired) and the mission duration is closer to the Lunar Mission of approx. *400s*, thermal loads are expected to drive the GMA functionality and design. In the favored case that the GMA design concept will be proofed in DM2 and the on-Earth demonstration *Oneiros*, this parameters will drive the design challanges of subsequent Developmen Tests

#### 6.3.0.1. Development Test Objectives  

The Overall Test Plan [RD11] will be updated as TVC is not part of the current version from the Preliminary Design Review. Hence, the objectives w.r.t. to the TVC are not yet defined on a system level. Some objectives, however, can be derived based on the current developoment state of the GMA from a component level and the requirements stated in [RD10].  

It must be noted that one objective does not necessarily represent a single test, and that multiple objectives can be
achieved during a single test run. Similarly, one objective might require multiple test runs before it is entirely fulfilled. 

**Thermal mapping** 
**Bearing lifetime prediction and measurement** 
**Wear of parts measurement and inspection**
**Loos of torque with load tracking of actuator loads w.r.t. to load cells measurements**
  
## 6.4. Qualification Test  

Qualification testing is performed after the design has reached a controlled and sufficiently mature configuration. It is conducted on a dedicated qualification engine or other approved flight-representative engine to demonstrate that the design complies with its specified requirements in the intended operational environments, including the applicable qualification margins. It is assumed that the objectives of the Qualification Tests are defined and executed at engine system level. Hence, the qualification testing objectives are elaborated in the Huracan Overall Test Plan [RD2].  

\clearpage  

# 7. Annex  
## 7.1. Instructions: Spherical Bearing Swaging Tool

![User instructions for swaging](<../WP3/figures/Pegasus_instructions bearing swaging.png>)  

![Anvil swaging](<../WP3/figures/Pegasus_instructions bearing swaging_Fig4.png>)  

![Gauging of swaged bearing](<../WP3/figures/Pegasus_instructions bearing swaging_Fig5.png>)

# 8. Acronym  

| **Acronym**  | **Definition**   |
|---|---|
|COTS |Commercial Off-The-Shelf|
|GMA  |Gimbal Mount Assembly|
|GSE  |Ground Support Equipment|  
|IGS |Ignition System|
|MAIT |Manufacturing, Assembly, Integration and Test|
|TVC |Thrust Vector Control|
: Acronyms

