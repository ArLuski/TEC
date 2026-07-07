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

[RD7] Nyx Moon - Huracan Development Logic / TEC-FRA-DOC-01004 / Issue 02  

[RD8] Gimbal Mount Assembly - Justification File/ Version 001  



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

The sequence of the assembly is described in this chapter. The subsequent description shall be accompanied during practical execution along side the dedicated 3D data (CAD-ID: 126703/01). 

The assembly is divided in two main steps (Figure 4).  

![GMA - Assembly steps](<../WP3/figures/GMA_assembly steps.png>){width=100%}  

In the **first step** (Figure 4, left), the Spherical Bearing *MS14103-10* is inserted into the Clevis Lug Head. Due to the interference fit  between the Inner Race of the Spherical Bearing and the Lug Head from *-0.0055 mm to +0.0202 mm*, a mounting force will be required. This force shall be centrically introduced by a hydraulic press through a customized Anvil (CAD-ID: 2020/01). The purpose of this customized GSE tool is to position the bearing so that it´s width is aligned with the width of the GMA Lug Head. In addition, the tool allows the mounting force to be transmitted through the outer race of the Spherical Bearing only and thus protect the PTFE-fabric liner from being damaged or worn prior engine operation. The anvil swaging of the bearing over housing is then executed following *Method 100* [RD5]. Further instruction details are to be extracted from the manual [RD4] or in chapter 8.1.

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

2. Development Phase: Detailed design phase using an iterative approach alongside testing of the Development Models. A total of four Development Models are tested as part of test campaigns: DM1 to DM4 [RD7]. Important to note is that the DM1-campaign already took place beginning 2026 without the GMA, but a rigid Thrust Structure. After passing the Derisking phase, the GMA will enter the Development Phase earliest in DM2.
   
3. Qualification Phase: Testing begins at the Final Design Key Point and continues up to the Ready for Flight
review to ensure the Huracan engine’s readiness for its first mission

## 6.2. Acceptance Test  

Acceptance Tests are performed on each manufactured part to verify conformity, workmanship, structural integrity, and basic functionality before assembly to a component and higher-level engine system testing later. After successful GMA component acceptance tests, the hardware proceeds to a subsystem testing in the *H05* campaign, which also encompasses the TVC-actuators and the bellows with representative routed and pressurized ducts. This campaign is understood as part of acceptance that is required for early derisking and entry of engine-level testing in the frame of Development Tests. 


### 6.2.1. Inspection  

Each GMA part will be inspected prior entering the acceptance tests. It consists of a visual inspection using
a microscope if required, as well as the measurement of main physical properties such as mass and main
dimensions. Material certificate and heat treatment checks, such as GD&T inspection according to specifications in manufacturing drawings are also reviewed during the incoming inspection. Among the custom machined parts, the main dimensions of the assembled COTS parts are to be inspected and documented in accordance with the standards specifications. 

**Sucess criteria**
• Surface: No cracks, scratches, dents, or signs of corrosion that may affect the part’s structural integrity.  

• Cleanliness: The parts are free from contaminants like dirt, grease, or debris  

• Material anomalies: Check for any visible signs of material inconsistency, such as discoloration, uneven texture,
porosities. Check also for conformity of material certificate, heat treatment and thermal/mechanical properties in accordance with assumptions during theoretical analysis  

• Accuracy of Dimensions and Tolerances: critical dimensions and tolerances (GD&T) match design specifications, ensuring that the part is within its specification

### 6.2.2. Proof Tests 

- No proof tests intended for bearing pull-through as shown in NAS0331
- Even though a quasi-static load test is desired, it won´t be part of Acceptance Testing due to limited capabilities to simulate the load and programmatic reasons.   

**Sucess criteria**

### 6.2.3. Functional Tests  

1. Proper assembly?
2. Force to be tracked for assembly of Lug-Bearing
3. Full gimbal-travel funcitonal test (Angular travel limits, Intereference
4. Breakaway and running torque 
6. End-stop and interference checks



## 6.3. Development Test  

Development tests are conducted during the design-maturation phase to build confidence in new designs and concepts aligned with the Overall Test Plan objectives on the engine system level in accordance to [RD2]. Their objectives are to:

- Characterize the behaviour and performance of the engine;
- Identify weaknesses in the materials, components, interfaces, or overall design;
- Validate and correlate analytical/numerical models;
- Investigate operating limits and off-nominal behaviour;
- Support the resolution of design issues; and
- Provide confidence that the final design can successfully complete enter the next Development stage and finally qualification.

Development-test conditions can extend beyond the normal design or operating range where this is necessary to identify credible weaknesses or design deficiencies. Development testing is iterative and can be performed concurrently with design modifications. However, successful development testing does not, by itself, constitute qualification unless the test article, configuration, test levels, durations, instrumentation, procedures, and success criteria satisfy all applicable qualification requirements.  

The current GMA represents the first design iteration within the project. During the development of the design, it could be shown, that parallel developments of adjacent components have an immediate and meaningful impact on the GMA design and its representativity for future development and qualification models. As shown in the Justification File [RD7] for instance, the GMA is not designed for thermal loads. This is given by the current design of the Thrust Dome that is a dependend of the Ignition System (IGS) design update and the mission duration of the on-Earth demonstrator *Oneiros* of less then *60s*. When the IGS design changes in favor of more compactness and mass reduction (to be expected) and the mission duration is closer to the Lunar Mission of approx. *400s*, thermal loads are expected to drive the GMA functionality and design. 

**Place Testing Objectives here**
- Thermal map of different positions as function of development
- Bearing lifetime
- Wear of parts
- Loos of torque
  
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
: Acronyms

