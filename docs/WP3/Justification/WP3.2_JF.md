---
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
  -  \usepackage{xcolor}
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
  - \fancyhead[R]{Gimbal Mount Assembly - Justification File - Version 001}
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
This document presents the Design Justification File for the Gimbal Mount Assembly (GMA). Its purpose is to explain the rationale behind the selected design and demonstrate that it meets the baseline requirements specified in [RD02]. It lists and describes the justification for:  

- Functional Design
- Thermal Design
- Mechanical Design

##  1.2. Reference
[RD1] A.Lukanowski - Gimbal Mount Assembly - Requirement Consolidation / Version 0 - Luebeck 2026  

[RD02] Gimbal Mount Assembly - Requirement Consolidation / Version 001  

[RD03] SKF Spherical Plain Bearings and Rod Ends / 2013  

[RD04] Bearings, Control System Components, and Associated Hardware Used in the Design and Construction of Aerospace Mechanical Systems and Subsystems / MIL-HDBK-5199 / 1997  

[RD05] RBC Aerospace FibriloidCR Series - Cryogenic Rated Plain Bearings: Sphericals, Rod Ends and Journals / 2024  

[RD06] SKF Aerospace Solutions / 2020  

[RD07] NASA Reference Publication 1228 / Fastener Design Manual / 1990  


\clearpage

# Functional Design  
## Chosen Tolerances and fits  
**Figure 1** shows a cross-sectional view in which all radial interfaces are color-coded. **Table 1** summarizes the dimensional limits and resulting diametral fit range for each mating outside-diameter/inside-diameter interface. Positive fit values indicate clearance, while negative values indicate interference.
  
![GMA - Radial tolerances color-coded](<../figures/GMA_tolerances_color code.png>){width=25%}  

| **Mating parts** | **Shaft (mm)** | **Hole (mm)** | **Resulting Fit (mm)** |
|---|---|---|---| 
| \textcolor{blue}{Bearing \& Lug}     |30.1498–30.1625 |30.1570–30.1700 |**-0.0055 to +0.0202**|
| \textcolor{brown!60!black}{Bolt \& Bearing}    |15.8369–15.8496 |15.8623–15.8750 |**+0.0127 to +0.0381**|
| \textcolor{red}{Bolt \& Clevis}    |15.8369–15.8496 |15.8623–15.8750 |**+0.0127 to +0.0381**|
| \textcolor{green!60!black}{Bolt \& Bushing}    |15.8369–15.8496 |15.8623–15.8750 |**+0.0127 to +0.0381**|
| \textcolor{black}{Bolt \& Spacer}     |15.8369–15.8496 |15.8750–15.902  |**+0.0254 to +0.0651**|
| \textcolor{purple}{Bushing \& Clevis} |19.9800–19.9930 |20.0000–20.0210 |**+0.0070 to +0.0410**|
: Radial tolerances and fits  

The selection of the commercial off-the-shelf (COTS) MS14103-10 spherical bearing and NAS6710DU29 bolt constrains the available bearing and bolt-shank dimensions. The dimensions of the corresponding mating bores were selected to provide the required assembly clearances. The resulting bolt-to-bore clearances are also consistent with established bearing-supplier recommendations, including those provided by *SKF* [RD03].  

To simplify assembly and inspection and to minimize the precautions required during integration, a common close-clearance fit is used for most bolt-to-bore interfaces. The exception is the transition fit between the GMA lug-head bore and the spherical-bearing outer ring. During bolt tightening, the clearance at the bolt interfaces allows the components to align and seat axially without radial binding.  

The only transition fit in the assembly is between the GMA Lug Head bore and the Spherical Bearing outer ring. This fit intentionally differs from the generic recommendation in the Defense Handbook [RD04], which specifies a nominal 0.001-inch clearance fit.  

In contrast to the generic recommendation, *SKF* [RD03] distinguishes between housing fits according to the housing material and the expected loading conditions. For steel/PTFE-fabric spherical bearings subjected to heavier loads or shock loading, SKF recommends a tighter housing fit. Applying the recommended *K7*-housing-bore tolerance to the outside-diameter limits of the *MS14103-10* Spherical Bearing results in a calculated fit range of **-0.0180 to +0.0197 mm**.  

Other bearing suppliers, including RBC Aerospace [RD05] and NHBB [reference required], recommend a transition fit of approximately -0.005 to +0.020 mm for self-lubricating spherical bearings. The selected GMA dimensions produce a fit range of -0.0055 to +0.0202 mm, which closely matches this recommendation. This fit was selected because the GMA is expected to experience high oscillatory loads during steady-state operation and transient shock loads during ignition, shutdown, and combustion-instability events.   

In the event of a interference of **-0.0055 mm** between Spherical Bearing and Lug, the clearance fit is expected to remain between the Bolt and Bearing. As a conservative screening calculation, assuming that the full outer-ring diametral compression were transferred directly to the bearing bore would leave 0.0072 mm (0.0127 mm - 0.0055 mm) of diametral bolt-to-bearing clearance.  

It should also be noted that a tighter housing fit can alter the installed bearing clearance and decrease the bearing friction coefficient at a given temperature, as described qualitatively for self-lubricating spherical bearings by *SKF* [RD06].  

![Load and temperature dependend evolution of bearing friction coefficient [RD06]](<../figures/SKF_bearing friction.png>){width=55%}  

  
## Tolerance stack-up analysis  

A tolerance stack-up analysis is conducted with the objective to keep tolerances as tight as possible to maintain the design compact, reduce the roll-error (pivot on x-axis) and comply the geometrical constraints given by COTS parts utilized. **Figure 3** shows four cases of tolerance stack-up analysis performed to estimate the minimum and maximum clearance under worst-case considerations (absolute extreme tolerance limits)  

![GMA tolerance stack-up](<../figures/GMA_tolerance stack.png>){width=50%}  

**Table 2** presents the related values calculated.

| **Stack-up** | **Nominal value (mm)** | **Max. value (mm)** | **Min. Value (mm)** |
|---|---|---|---| 
| 1 |0.3 |0.6 |0.1|
| 2 |0|0.0854 |0.015|
| 3 |1.225 |1.425 |0.904|
| 4 |0.699 |1.055 |0.395|
: Worst-Case Tolerance Analysis

## Preload of NAS-bolt  

The Castellated Nut shall be tightened until all components of the axial joint stack are fully seated and unacceptable axial play is eliminated. From this seated condition, the nut shall be advanced in the tightening direction only to the first position at which a castellated slot aligns with the bolt cross-hole, after which the Cotter Pin shall be installed. 

Assuming the specified the thread *0.6250-18 UNJF-3A*, the pitch is  
$p=\frac{1}{18}\,\text{inch}=1.41\,\text{mm}$  

For a castellated nut with six equally spaced slots, the maximum angular advance required for alignment is 60°. The corresponding maximum relative axial thread advance is  

 a pitch of 1/18 inch (1.41 mm). Taking into acoount that the Castellated Nut *MS9358-016* contains six grooves, the spacing between grooves is 60 °. Roughly, for an angle of rotation of 60 ° with the wrench, the relative thread advance is estimated by:

$\Delta$s$=\frac{60°}{360°}\ * 1.41 mm=0.235\,\text{mm}$ 

This value represents the maximum relative nut advance after seating. It shall not be interpreted directly as bolt elongation because the imposed displacement is distributed between bolt extension, compression of the joint stack, and local deformation of the threads and bearing surfaces.

When an adjustment of 0.235 mm is applied in the ANSYS bolt-pretension model, the calculated preload is 63.4 kN. This result includes the modeled stiffness and contact behaviour of the bolt and clamped components but does not account for installation scatter, embedment, relaxation, or temperature effects. 

The analysis with a friction coefficient of 0.2 indicates that this preload significantly changes the lateral load path. Like **Figure??** demonstrates, a substantial portion of the lateral load is transfered through friction rathern than through the intended bolt, bearing-inner-member, and clevis-hole contact path. 

![Frictionall Stresses with/withoug preload of NAS-bolt(<../figures/FEM_NASbolt preload friction stress.png>){width=60%}  

In summary, the minimum torque is to be chosen so that axial play is eliminated. The maximum torque is estimated so the main engine operational thrust force is not transmitted through the friction as exemplarily shown above. Specifically for the on-Earth demonstrator *Oneiros* a minimum Thrust level of 6 kN is maintained through the entire duration as shown by the Guidance Navigation Control simulation (GNC) in **Figure??**. Taking into account the Alternative Torque Formula for quick bolt torque calculations [RD07], a to

![[GNC-simulation - Thrust requirement over Time]](<../figures/GNC_thrust level.png>)]{width=50%}  




# Thermal Analysis  
**Generic Boundary Conditions** 



# Mechanical Analysis  
## Bearing Lifetime
  - Show first how size was determined @MIL-HDBK-1599 - 201.143
  - Show computed lifetime according SKF
  - Discuss results
## Bolt, Lug, Clevis
  - Preliminary assesment Ro/Ma
  - Show simplified assumptions and analytical result
  - Show numerical result
## Static Structural  
## Prelminary Analysis
### Bolt, Lug, Clevis  

### Spherical Bearing: Liner Stiffness  

## GMA Static-Structural Analysis
  - 0° with Thrust load and Acceleratoin
  - Worst case angles (pitch/yaw)
  - Discuss results
    - Modelling of liner (boded)

# Conclusion 
\clearpage  


# Annex  

## Tolerance Stack Analyis  


## Boundary Conditions Thermal Analysis 

## Boundary Conditions Static Structural Analysis  

## Tolerance Stack Analyis


\clearpage 
# 3. Acronym List  
The acronyms used in this document are listed below.  

| **Acronym**  | **Definition**   |
|---|---|
|COTS|Commercial Off-The-Shelf|
|GNC|Guidance Navigation Control|
|GMA|Gimbal Mount Assembly|

