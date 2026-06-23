---
title: |  
  **Gimbal Mount Assembly**  
  Definition File
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
The definition file serves as the identity card of the Gimbal Mount Assembly (GMA), detailing its intended capabilities and interactions with other systems. The document aims to provide a thorough understanding of the following key aspects:

• Overview of the components that constitute the GMA and their main purposes  
• Description of the mechanical characteristics  
• Identification of the operating characteristics and the main performance metrics   
• Preliminary cost estimation  
• Design recommendations for adjacent parts

##  1.2. Reference

[RD1] Nyx Moon - Huracan Development Logic / TEC-FRA-DOC-2024-01004 / Issue 02 

[RD2] Gimbal Mount Assembly - Requirement Consolidation / Version 0 

[RD3] Gimbal Mount Assembly - Trade-Off Report / Version 0 

[RD4] Gimbal Mount Assembly - Interface Control Document / Version 0 

[RD5] Gimbal Mount Assembly - Justification File / Version 0 


\clearpage

# 2. GMA Overview
## 2.1. Engine system context  
The development logic of the Huracan engine system, as presented during the Preliminary Design Review (PDR), features a rigid thrust structure that interfaces the main engine with the vehicle [RD1]. Based on this logic, GNC maneuvers were originally intended to be performed by a Reaction Control System (RCS).

For the on-Earth demonstrator *Oneiros*, which shall be driven by the Huracan engine, pitch and yaw control is planned to be realized by a Thrust Vector Control (TVC) system. The TVC system steers the vehicle by physically pivoting, or gimballing, the main engine in order to vector the thrust. Therefore, the main mechanical components of the TVC system are the Gimbal Mount Assembly (GMA) and two actuators. 

This Definition File focuses exclusively on the development of the Gimbal Mount Assembly (GMA).

In the figure below, the GMA and its position within the engine layout are shown. The GMA is attached to a Thrust Dome, which interfaces with the Injection Head (IH). This interface provides clearance and accessibility for the centrally located Ignition System (IGS) and its periphery. The upper end of the GMA is connected to the Thrust Frame Beams, which are individually connected to the GMA in a 90°-clocked configuration.

![GMA in engine system](<../figures/GMA_engine context.png>){ width=55% }

## 2.2. Role of the GMA in the Engine System  
The main role of the GMA is to provide the structural and kinematic connection between the engine’s Thrust Chamber Assembly (TCA) and the vehicle structure, while allowing controlled angular deflection of the engine.

The GMA does not directly generate thrust, specific impulse, or combustion performance. However, it is strongly influenced by engine-level performance and configuration, since these parameters define the loads, deflections, actuator forces, alignment requirements, and environmental conditions that the assembly must withstand.

The GMA shall therefore be considered as an interface and primary mechanical load-path component between the engine and the vehicle. It transmits nominal thrust loads of 15 kN in vacuum and 10 kN under atmospheric conditions. In addition to transmitting the nominal loads, the GMA shall provide an operational gimbal capability of ±10° per axis in pitch and yaw. Further requirements are shown in the Requirement Consolidation [RD2].

# 3. GMA Design Definition

## 3.1. Assembly architecture & Design Philosophy 

Breaking down the assembly from the engine system to the GMA and its direct adjacent parts, the figure below shows the GMA connected with the Thrust Dome (bottom) and the Thrust Frame Beams (above). The Thrust Dome and the Thrust Frame Beams are transperantly illustrated as those are not within the scope of this development. Neverthless, design recommendations for these specific parts have been made in a subsequent chapter.  

![GMA architecture](<../figures/GMA architecture.png>){width=65%}  

The design philosophy is aligned with the Trade-Off criteria described in [RD3]. To achieve design of the GMA that is *safe, simple and achievable*, the objective is to reduce the part count and include as much COTS parts as possible. As a result the final GMA design features 8 parts in total, 4x COTS and 4x custom made (figure below). Military and aerospace standards related machine parts are chosen for COTS parts due to their guaranteed material properties, tight tolerances and controlled manufacturing / inspection procceses. Imperial units will be compromised for this project due cheaper and faster sourcing of those parts. 

![COTS parts in the GMA](<../figures/GMA explosion cots.png>){width=40%}  

## 3.2. Part breakdown, material and mass

The image and subsequent table below illustrates the components and its designated material in an isometric and cross-section view. For the NAS-bolt specifically it is to be noted, that the finish described by the letter *U* (bolt passivated) is driven by the availibilty of this specific bolt size in the market. The passivation is not required for the function of the assembly per se.

 ![GMA isometric view and cross section](<../figures/GMA_isometric_cross section.png>){ width=90% }  

| **Number** | **CAD-ID** | **Designation** | **Material** | **Mass (kg)** |
| :---: | :---: | :--- | :---: | :---: |
| 1 | 126749/01 | GMA Clevis Head | 17-4PH - H900 | 0.864 |
| 2 | 3489/01 | COTTER Pin MS24665-374 | AISI 302 or 304 | 0.0022 |
| 3 | 126711/01 | GMA GMA Bushing | 17-4PH - H900 | 0.0147 |
| 4 | 3423/01 | BOLT NAS6710DU29 | CRES A286 | 0.1316 |
| 5 | 3437/01 | Nut MS9358-16 | CRES A286 | 0.0386 |
| 6 | 126707/01 | GMA GMA Spacer | 17-4PH - H900 | 0.0003 |
| 7 | 3489/01 | BEARING MS14103-10 | 330C / 17-4PH | 0.1089 |
| 8 | 124890/01 | GMA Lug Head | 17-4PH - H900 | 0.381 |
| **Total mass** |  | |  | **1.544** |
: Total mass of main parts  

Taking into account the bolts, washers, nuts and pins, an additional CAD-mass of 0.212 kg is to be considered. Hence, the total mass is approximatly **1.8 kg**, which is **64%** less then the max. from the given requirement [RD2]. Further and detailed descriptions of the interface connections is stated in the Interface Control Document (ICD) of the GMA [RD3]. 

## 3.3. Tolerances and fits

The choice of geometrical fits between mating diameters is driven by COTS parts utilized in the design for the Plain Bearing and Bolt and their fixed dimensions, recommendations by standards for BEARING and GMA Lug Head, functionality and flexibility during MAIT procedures. 

| **Parts** | **Shaft (mm)** | **Hole (mm)** | **Resulting tolerance (mm)** |
|:---:|:---:|:---:|:---:|
| BEARING & LUG | 30.1498–30.1625 | 30.1570–30.1700 | **-0.0055 to +0.0202** |
| BOLT & BEARING | 15.8369–15.8496 | 15.8623–15.8750 | **+0.0127 to +0.0381** |
| BOLT & CLEVIS | 15.8369–15.8496 | 15.8623–15.8750 | **+0.0127 to +0.0381** |
| BOLT & BUSHING | 15.8369–15.8496 | 15.8623–15.8750 | **+0.0127 to +0.0381** |
| BOLT & SPACER | 15.8369–15.8496 | 15.8623–15.8750 | **+0.0127 to +0.0381** |
| BUSHING & CLEVIS | 19.9800–19.9930 | 20.0000–20.0210 | **+0.0070 to +0.0410** |
: Tolerances and fits  

# 4. Functional characteristics 
An overview of the main GMA´s parts function is shown in the table below. The part numbering and designation is associated to figure 4.   

| **Number** | **Designation** | **Function** |
| :---: |:--- | :---: | 
| 1 | GMA Clevis Head | Transfers loads into the thrust frame structure; provides centering and positioning of the lug interface; supports engine handling and positioning of instrumentation interfaces
| 2 | COTTER PIN MS24665-374| Provides positive locking of the nut and prevents unintended loosening
| 3 | GMA GMA Bushing | Provides axial positioning of the lug/bearing interface and supports axial load transfer between adjacent components
| 4 | BOLT NAS6710DU29| Transfers shear and bending loads through the clevis/lug joint; provides axial and radial positioning of the connected parts
| 5 | Nut MS9358-16| Retains the bolt in the clevis/lug joint and maintains joint assembly integrity
| 6 | GMA Spacer | Provides centered positioning of the lug/bearing assembly and maintains the required axial spacing
| 7 | BEARING MS14103-10 | Supports radial and axial loads while allowing angular displacement in pitch and yaw
| 8 | GMA Lug Head | Transfers loads between the bearing and engine interface; provides bearing support and mechanical stop functionality
: GMA parts and function


## 4.1. Mechanical Limits

The mechanical limits can be categorized as stability related, geometrical and kinematical limits. 

Stability limits of the GMA are driven by the weakest and most sensitive part. This will be elaborated in detail in the Justification File [RD4].

Geometrical and kinematical limits are given by the nature of the chosen bearing´s capability to tilt. For the self lubricating plain bearing *MS14103-10*, the max. angle of tilt is 12°. Exceeding this value may result in a reduction of the bearing lifetime, additional bending of the bolt etc. To protect the bearing, a mechanical stop feature is considered in the design of the GMA Clevis Head as shown in the figure below, where the GMA Lug is tilted by nominally 12° w.r.t. the GMA Clevis Head.

![GMA - yaw=12°, pitch=0°](<../figures/GMA cross section_ yaw12deg.png>){width=65%}

# 5. Cost assessment 

For the preliminary cost assessment, the custom made parts are  assessed by *makerverse.com*, while the costs of the COTS parts are estimated by e.g. *adeptfasteners.com* and *LMFIXATIONS.com* and *militaryfasteners.com*. The unit prices shown below are based on a minimum purchase of max. 10 units. The price is subject to an average delivery time of up to 14 to 20 business days.

| **Part**| **CAD-ID** | **Material** | **Cost (€/unit)** |
| ------ | ----- | ------- |------- |
| GMA Clevis Head |126749/01| 17-4PH - H900 |532 |
| GMA Lug Head |124890/01| 17-4PH - H900 | 241 |
| GMA GMA Bushing |126711/01| 17-4PH - H900 | 35 |
| GMA GMA Spacer |126707/01| 17-4PH - H900 |30 |
| BEARING MS14103-10 |126707/01| 17-4PH - H900 |50 |
| Bolt NAS6710DU29 |3423/01| CRES A286| 50 |
| Nut MS9358-16 |3437/01| CRES A286| 88 |
| PIN MS24665-374 |3489/01| CRES A286| 9 |
| **Total cost** |  |  |**1035**|
: Cost estimation

In addition to the total costs estimated above, a specific staking tool is needed to fix the bearing outer race in the GMA Lug Head. The estimated price per unit is approx. 260 €. Thus, the total price is including the tool is **1295 €**.  

# 6. Design recommendation for adjacent parts  
As mentioned in the chapters before, the GMA development does not include the interfacing parts to the engine and the vehicle. Nevertheless, since these are not finally designed yet, but directly interfacing with the GMA, it is worth to show a design suggestion from the perspective of the GMA development. 

**Thrust Frame Beam**  
The GMA Clevis Head is designed so that four seperate structure parts can be fixed independently in a Quadpod-configuration. These Thrust Frame Beams are primarily designed to  transmit the engine´s thrust into the vehicle structure. The secondary function is to provide the possibility to attach additional components and instrumentation. The suggested dimensions of the I-beam are shown in the figure.

![Thrust Frame Beam dimensions](<../figures/Thrust Beam.png>){width=45%}  

**Thrust Dome**  
The Thrust Dome´s main function is to provide space to accommodate the IGS and its peripherical attachments, but also transmit the total thrust and thermal loads from the IH into the GMA. It is designed as an axially symmetrical body with radial cut-outs for space and accessibility to the IGS. The material is considered to be 17-4PH - H900. The main suggested dimensions are shown below. The centering feature is designed in a 90-clocked configuraton of as a longitudinal groove. The function if the groove is to precisely position Thrust Dome on the IH w.r.t. the lateral axis, but also its clocking while considering the thermal contraction of the male part (e.g. pins in the IH)

![Thrust Dome design](<../figures/Thrust Dome.png>){width=50%}  

# 7. Acronym List  
The acronyms used in this document are listed below.  

| **Acronym**  | **Definition**   |
|---|---|
|GMA|Gimbal Mount Assembly|
|IGS|Ignition System|
|IH|Injection Head|
|PDR| Preliminary Design Review 
|RCS|Reaction Control System|
|TCA|Thrust Chamber Assembly|
|TVC|Thrust Vector Control|
: Acronyms