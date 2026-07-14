---
title: |  
  **Gimbal Mount Assembly**  
  Definition File
author: Artjom Lukanowski on behalf of The Exploration Company SAS     
version: "001"
date: "Version 000 created on \\today"
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
  - \fancyhead[R]{Gimbal Mount Assembly - Definition File - Version 001}
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
The Definition File serves as the identity card of the Gimbal Mount Assembly (GMA), detailing its intended capabilities and interactions with other systems. The document aims to provide a thorough understanding of the following key aspects:

• Overview of the components that constitute the GMA and their main purposes  
• Description of the functional mechanical characteristics   
• Design recommendations for adjacent parts  
• Preliminary cost estimation  

##  1.2. Reference

[RD01] Nyx Moon - Huracan Development Logic / TEC-FRA-DOC-01004 / Issue 02 

[RD02] Gimbal Mount Assembly - Requirement Consolidation / Version 001 

[RD03] Gimbal Mount Assembly - Trade-Off Report / Version 001 

[RD04] Gimbal Mount Assembly - Interface Control Document / Version 001 

[RD05] Gimbal Mount Assembly - Justification File / Version 001 


\clearpage

# 2. GMA Overview  
## 2.1. Context to Engine System   
The development logic of the Huracan engine system, as presented during the Preliminary Design Review (PDR), features a rigid thrust structure that interfaces the main engine with the vehicle [RD1]. Based on this logic, GNC maneuvers were originally intended to be performed by a Reaction Control System (RCS).

For the on-Earth demonstrator *Oneiros*, which shall be driven by the Huracan engine, pitch and yaw control is planned to be realized by a Thrust Vector Control (TVC) system. The TVC system steers the vehicle by physically pivoting, or gimballing, the main engine in order to vector the thrust. Therefore, the main mechanical components of the TVC system are the GMA and two actuators. 

This Definition File and all associated documents focus exclusively on the development of the GMA.

The figure below shows the GMA and its position within the engine layout. The GMA is attached to a Thrust Dome, which interfaces with the Injection Head (IH). The upper end of the GMA is connected to the Thrust Frame Beams, which are individually attached to the GMA in a 90°-clocked configuration.

![GMA in engine system](<../figures/GMA_engine context.png>){ width=55% }

## 2.2. Role of the GMA in the Engine System  
The main role of the GMA is to provide the structural and kinematic connection between the engine’s Thrust Chamber Assembly (TCA) and the vehicle structure, while allowing controlled angular deflection of the engine.

The GMA does not directly generate thrust, specific impulse, or combustion performance. However, it is strongly influenced by engine-level performance and configuration, since these parameters define the loads, deflections, actuator forces, alignment requirements, and environmental conditions that the assembly must withstand.

The GMA shall therefore be considered as an interface and primary mechanical load-path component between the engine and the vehicle. It transmits nominal thrust loads of 15 kN in vacuum and 10 kN under atmospheric conditions. In addition to transmitting the nominal loads, the GMA shall provide an operational gimbal capability of ±10° per axis in pitch and yaw. Further requirements are shown in the Requirement Consolidation [RD2].

# 3. GMA Design Definition

## 3.1. Assembly Architecture & Design Philosophy 

Breaking down the engine assembly to focus on the GMA and its directly adjacent parts, the figure below shows the GMA connected to the Thrust Dome at the bottom and the Thrust Frame Beams above. The Thrust Dome and Thrust Frame Beams are shown transparently because they are outside the scope of this development. Nevertheless, design recommendations for these components are provided in a subsequent chapter. 

![GMA architecture](<../figures/GMA architecture.png>){width=60%}  

The design philosophy is aligned with the trade-off criteria described in [RD3]. To achieve a GMA design that is *safe, simple, and achievable*, the primary objectives are to minimize the number of parts and maximize the use of commercial off-the-shelf (COTS) parts. As a result, the final GMA design consists of eight parts: four COTS parts and four custom-made parts. The following figure shows the COTS parts used in the GMA.

Machined parts manufactured in accordance with military and aerospace standards were selected as COTS parts because of their guaranteed material properties, tight tolerances, and controlled manufacturing and inspection processes. The use of imperial units is accepted for some parts in this project because they can be sourced more quickly and at a lower cost.  

![COTS parts in the GMA](<../figures/GMA explosion cots.png>){width=40%}  

## 3.2. Part Breakdown, Materials and Mass

The image and the subsequent table illustrate the parts and their designated materials in isometric and cross-sectional views.

The GMA forms a double-shear clevis joint in which the GMA Lug Head supports the staked outer race of a self-lubricating Plain Bearing. The Bearing inner race is centered within the GMA Clevis Head by a Spacer and clamped against the Bushing by the preload of the NAS-bolt. A castellated nut contacts the outer surface of the GMA Clevis Head, while a Cotter Pin prevents the nut from loosening and maintains the axial position of the stacked components.

The two Clevis Ears interface with the NAS-bolt on one side and the GMA Bushing on the other. Their bores have different diameters and clearance fits to ensure controlled seating and clamping of the axially stacked components while maintaining the centered position of the GMA Lug Head between the Clevis Ears.  

The “U” suffix in the NAS-bolt designation identifies the available passivated finish. This finish is driven by market availability and is not functionally required by the assembly.  

 ![GMA isometric view and cross section](<../figures/GMA_isometric_cross section.png>){ width=90% }  

| **Number** | **CAD-ID** | **Designation** | **Material** | **Mass (kg)** |
|---|---|---|---|---|
| 1 | 126749/01 |GMA Clevis Head              |17-4PH - H900    |0.864  |
| 2 | 3489/01   |Cotter Pin MS24665-374       |AISI 302 or 304  |0.0022 |
| 3 | 126711/01 |GMA Bushing                  |17-4PH - H900    |0.0147 |
| 4 | 3423/01   |Bolt NAS6710DU29             |A286             |0.1316 |
| 5 | 3437/01   |Nut MS9358-16                |A286             |0.0386 |
| 6 | 126707/01 |GMA Spacer                   |17-4PH - H900    |0.0003 |
| 7 | 19156/01  |Bearing MS14103-10           |330C / 17-4PH    |0.1089 |
| 8 | 124890/01 |GMA Lug Head                 |17-4PH - H900    |0.381  |
| **Total mass** |  | |  | **1.544** |
: Total mass of main parts  

Taking into account the additional bolts, washers, nuts, and pins, an additional CAD mass of 0.2 kg must be considered. The total mass is therefore approximately **1.7 kg**, which is **64 %** lower than the maximum mass specified in requirement [RD2]. Further details of the interface connections are provided in the GMA Interface Control Document (ICD) in [RD4].  

## 3.3. Tolerances and Fits

The selection of dimensional fits between mating cylindrical surfaces is governed by the fixed dimensions of the COTS parts used in the design. It also considers the fit recommendations specified by the applicable standards for the bearing and the GMA Lug Head, as well as the functional requirements of the assembly and the flexibility required during Manufacturing, Assembly, Integration, and Testing (MAIT). 

| **Parts** | **Shaft (mm)** | **Hole (mm)** | **Resulting Fit (mm)** |
|---|---|---|---| 
| Bearing & Lug     |30.1498–30.1625 |30.1570–30.1700 |**-0.0055 to +0.0202**|
| Bolt & Bearing    |15.8369–15.8496 |15.8623–15.8750 |**+0.0127 to +0.0381**|
| Bolt & Clevis     |15.8369–15.8496 |15.8623–15.8750 |**+0.0127 to +0.0381**|
| Bolt & Bushing    |15.8369–15.8496 |15.8623–15.8750 |**+0.0127 to +0.0381**|
| Bolt & Spacer     |15.8369–15.8496 |15.8750–15.902  |**+0.0254 to +0.0651**|
| Bushing & Clevis  |19.9800–19.9930 |20.0000–20.0210 |**+0.0070 to +0.0410**|
: Tolerances and fits  

# 4. Functional and mechanical characteristics 

## 4.1. Generic functional characteristics
An overview of the functions of the main GMA parts is provided in the table below. The part numbers and designations correspond to those shown in Figure 4.

| **Number** | **Designation** | **Function** |
|---|---|---| 
| 1 | GMA Clevis Head | Transfers loads into the thrust frame structure; provides centering and positioning of the lug interface; supports engine handling and positioning of instrumentation interfaces
| 2 | Cotter Pin MS24665-374| Provides positive locking of the nut and prevents unintended loosening
| 3 | GMA Bushing | Provides axial positioning of the lug/bearing interface and supports axial/radial load transfer between adjacent components
| 4 | Bolt NAS6710DU29| Transfers shear and bending loads through the clevis/lug joint; provides axial and radial positioning of the connected parts
| 5 | Castellated Nut MS9358-16| Retains the bolt in the clevis/lug joint and maintains joint assembly integrity
| 6 | GMA Spacer | Provides centered positioning of the lug/bearing assembly and maintains the required axial spacing
| 7 | Bearing MS14103-10 | Supports radial and axial loads while allowing angular displacement in pitch and yaw
| 8 | GMA Lug Head | Transfers loads between the bearing and engine interface; provides bearing support and mechanical stop functionality
: GMA Parts and Functions

## 4.2. Chosen functional and mechanical characteristics

The GMA Lug Head and Clevis Head incorporate several specific mechanical features that are worth highlighting.

![Chosen Featurs of GMA Parts](<../figures/GMA features.png>){ width=60% }  

The GMA Clevis Head consists of two Clevis Ears connected by a horizontal flange. A central rectangular **Vertical Support** carries transverse loads from the angled Thrust Frame Beams and provides four support surfaces spaced 90° apart for precise, independent attachment. Further details are specified in the ICD [RD4]. 

The GMA Clevis Head contains two **Mechanical Stops** that limit the oscillation angle of the GMA Lug Head about the axis perpendicular to the NAS-bolt axis (z-axis; see Figure 2). These geometric features are intended to prevent the maximum permissible oscillation angle of the Bearing *MS14103-10* from being exceeded. The figure below illustrates the kinematic limit, with the GMA Lug Head tilted nominally by 12° relative to the GMA Clevis Head.

![GMA at 12° Yaw and 0° Pitch](<../figures/GMA cross section_ yaw12deg.png>){width=40%}  
  
The GMA Clevis Head features a raised **Clevis Extension** beneath the castellated nut. It accommodates the commercially available NAS-bolt length, aligns the nut slots with the bolt’s cross-drilled hole for cotter-pin locking, and uses an enlarged bore to prevent the threaded bolt section from carrying transverse shear or bending loads.  

A total of four **Anti-Roll Features** are incorporated into the design of the GMA Lug Head. Their purpose is to minimize relative rotation of the engine about the roll axis (z-axis, Figure 2) under all gimbal-angle conditions. Therefore, the clearance between these features and the nearest surface of the clevis is kept as small as possible.   

The GMA design uses two different **Clevis Bore Holes**. The smaller bore is in direct contact with the NAS-bolt, whereas the larger bore provides a clearance fit around the GMA Bushing. This clearance allows the axially clamped components to seat against one another in a controlled manner during bolt tightening.  

# 5. Design Recommendations for Adjacent Parts 
As mentioned in the previous chapters, the GMA development does not include the interfacing parts on the engine side and the vehicle side. Nevertheless, since these parts have not yet been finalized and directly interface with the GMA, it is useful to present design suggestions from the perspective of the GMA development.

**Thrust Frame Beam**  
The GMA Clevis Head is designed to allow four separate structural members to be attached independently in a quadpod configuration. These Thrust Frame Beams are primarily intended to transmit the engine thrust into the vehicle structure. Their secondary function is to provide attachment points for additional components and instrumentation. The suggested dimensions of the I-beam are shown in the figure below. The chosen material is EN AW-7075 T6. 

![Thrust Frame Beam dimensions](<../figures/Thrust Beam.png>){width=45%}  

**Thrust Dome**  
The main function of the Thrust Dome is to provide space to accommodate the IGS and its peripheral attachments, while also transmitting the total thrust and thermal loads from the IH to the GMA. It is designed as an axially symmetric body with radial cut-outs to provide space and accessibility for the IGS. The proposed material is 17-4PH - H900.

The main suggested dimensions are shown below. The centering feature is designed as a longitudinal groove in a configuration clocked at 90° intervals. The function of this groove is to precisely position the Thrust Dome on the IH with respect to the lateral axis and to define its clocking, while accounting for the thermal contraction of the mating male features, such as pins on the IH.

![Thrust Dome design](<../figures/Thrust Dome.png>){width=45%} 

# 6. Preliminary cost assessment 

For the preliminary cost assessment, the custom-made parts were quoted through makerverse.com, while the costs of the COTS parts were estimated using prices from suppliers such as *adeptfasteners.com, lmfixations.com, and militaryfasteners.com*. The unit prices shown below are based on order quantities of up to 10 units. The quoted prices are associated with estimated delivery times of approximately 14 to 25 business days.

| **Part**| **CAD-ID** | **Material** | **Cost (€/unit)** |
| ------ | ----- | ------- |------- |
| GMA Clevis Head             |126749/01  |17-4PH - H900    |273|
| GMA Lug Head                |124890/01  |17-4PH - H900    |195|
| GMA Bushing                 |126711/01  |17-4PH - H900    |40|
| GMA Spacer                  |126707/01  |17-4PH - H900    |31|
| Bearing MS14103-10          |19156/01  |330C/17-4PH       |50|
| Bolt NAS6710DU29            |3423/01    |A286             |50|
| Castellated Nut MS9358-16   |3437/01    |A286             |88|
| Cotter Pin MS24665-374      |3489/01    |AISI 302 or 304  |9|
| **Total cost**              |           |                 |**736**|
: Cost assessment  

In addition to the estimated costs listed above, a dedicated staking tool is required to secure the outer race of the bearing in the GMA Lug Head. This tool costs approximately € 260. Additional quality-assurance costs for the manufactured parts are estimated at € 500. Therefore, the total estimated cost of one functional GMA unit, including tooling and quality-assurance expenses, is **€ 1,496**.

\clearpage

# 7. Acronym List  
The acronyms used in this document are listed below.  

| **Acronym**  | **Definition**   |
|---|---|
|COTS |Commercial Off-The-Shelf|
|GMA  |Gimbal Mount Assembly|
|ICD  |Interface Control Document|
|IGS  |Ignition System|
|IH   |Injection Head|
|MAIT |Manufacturing, Assembly, Integration, and Testing|
|PDR  |Preliminary Design Review 
|RCS  |Reaction Control System|
|TCA  |Thrust Chamber Assembly|
|TVC  |Thrust Vector Control|
: Acronyms