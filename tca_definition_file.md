---
title: Huracan - TCA Definition File
identifier: TEC-FRA-DOC-2024-01141
authors: 
- Tomás Cruz
- Pierre Morin
configurations:
  reqs-huracan: latest
  acronyms:
      AM: Additive Manufacturing
          CF: Cost File
              CHF: Critical Heat Flux
                  CT: Computed Tomography
                      DED: Direct Energy Deposition
                          DF: Definition File
                              DM: Development Model
                                  DPPF: Relative Pressure Drop Fuel (MFV+injector) 
                                      DPPIF: Relative Pressure Drop Injector Fuel 
                                          DPPIO: Relative Pressure Drop Injector Oxidizer 
                                              DPPO: Relative Pressure Drop Oxidizer (MOV+injector) 
                                                  DPRC: Pressure Drop Regenerative Circuit 
                                                      DTRC: Temperature increase Regenerative Circuit
                                                          HF: High Frequency
                                                              HTD: Heat Transfer Deterioration
                                                                  IGS: Ignition System
                                                                      IH: Injector Head
                                                                          ISP_LOSS_COOLING: Isp loss due to film cooling
                                                                              ISP_SL: engine ISP Sea Level
                                                                                  ISP_VAC: engine ISP VACuum
                                                                                      ISPCC_SL: Isp Combustion Chamber Seal Level
                                                                                          ISPCC_VAC: Isp Combustion Chamber Vacuum
                                                                                              JF: Justification File
                                                                                                  LF: Low Frequency
                                                                                                      LPBF: Laser Powder Bed Fusion
                                                                                                          MCC: Main Combustion Chamber
                                                                                                              MFCI: Mass flow Fuel regenerative Circuit Inlet
                                                                                                                  MFCO: Mass flow Fuel regenerative Circuit Outlet
                                                                                                                      MFII: Mass flow Fuel Injector Inlet
                                                                                                                          MFIO: Mass flow Fuel Injector Outlet
                                                                                                                              MOII: Mass flow Oxidizer Injector Inlet
                                                                                                                                  MRC: Mixture Ratio Combustion chamber
                                                                                                                                      NA: Not Applicable
                                                                                                                                          NEL: Nozzel Extension Long
                                                                                                                                              NES: Nozzle Extension Short
                                                                                                                                                  PCC: Pressure Combustion Chamber
                                                                                                                                                      PFCI: Pressure Fuel regenerative Circuit Inlet
                                                                                                                                                          PFCO: Pressure Fuel regenerative Circuit Outlet
                                                                                                                                                              PFIHI: Pressure Fuel Injector Head Inlet
                                                                                                                                                                  PFII: Pressure Fuel Injector (dome) Inlet
                                                                                                                                                                      PFIO: Pressure Fuel Injector Outlet
                                                                                                                                                                          POIHI: Pressure Oxidizer Injector Head Inlet
                                                                                                                                                                              POII: Pressure Oxidizer Injector (dome) Inlet
                                                                                                                                                                                  RC: Regenerative Circuit
                                                                                                                                                                                      TFCI: Temperature Fuel regenerative Circuit Inlet
                                                                                                                                                                                          TFCO: Temperature Fuel regenerative Circuit Outlet
                                                                                                                                                                                              TFIHI: Temperature Fuel Injector Head Inlet
                                                                                                                                                                                                  TFII: Temperature Fuel Injector Inlet
                                                                                                                                                                                                      TFIO: Temperature Fuel Injector Outlet
                                                                                                                                                                                                          THRUST_SL: THRUST Seal Level
                                                                                                                                                                                                              THRUST_VAC: THRUST VACuum
                                                                                                                                                                                                                  TOIHI: Temperature Oxidizer Injector Head Inlet
                                                                                                                                                                                                                      TOII: Temperature Oxidizer Injector Inlet
                                                                                                                                                                                                                          TS: Technical Specification
                                                                                                                                                                                                                              TW_MAX: MAXimum hot-gas side Wall Temperature
                                                                                                                                                                                                                                  VCD: Verification Control Document
                                                                                                                                                                                                                                  ---

                                                                                                                                                                                                                                  <!---
                                                                                                                                                                                                                                  |||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||
                                                                                                                                                                                                                                  ATTENTION:
                                                                                                                                                                                                                                  when talking about simulations, it is important to differentiate between the development model and the flight like model
                                                                                                                                                                                                                                  For IH and MCC there is not much difference because current designs are close to flight like
                                                                                                                                                                                                                                  For IS and NE there can be significant differences between development and flight design
                                                                                                                                                                                                                                  Ideally, we should present the flight like. If we have both we can present both. If we do not have both, we mention
                                                                                                                                                                                                                                  that the analysis was done for a development model
                                                                                                                                                                                                                                  -->


                                                                                                                                                                                                                                  ## Introduction

                                                                                                                                                                                                                                  ### Scope

                                                                                                                                                                                                                                  The definition file serves as the identity card of the Thrust Chamber Assembly (TCA), detailing its intended capabilities and interactions with other systems. The document aims to provide a thorough understanding of the following key aspects: 

                                                                                                                                                                                                                                  - Overview of the components that constitute the TCA and their main purposes
                                                                                                                                                                                                                                  - Description of the underlying principles of thrust production and the main physical phenomena that govern the behavior of the TCA
                                                                                                                                                                                                                                  - Identification of the operating envelope and the main performance metrics such as thrust, efficiency and ISP
                                                                                                                                                                                                                                  - Description of the mechanical characteristics and interaction with the rest of the engine 
                                                                                                                                                                                                                                  
### Reference

- [RD1] TEC-FRA-DOC-2024-01142 - TCA Justification File
- [RD2] TEC-FRA-DOC-2024-01145 - TCA Development Logic
- [RD3] TEC-FRA-DOC-2024-01146 - TCA Overall Test Plan
- [RD4] DLR - ALM Swirl Element Test Report - 2022-12-23
- [RD5] TEC-FRA-DOC-2023-00066 - TCA1 Campaign PTR
- [RD6] TEC-FRA-DOC-2024-00020 - TCA2 Campaign PTR
- [RD7] TEC-FRA-DOC-2024-01147 - TCA Manufacturing, Assembly, Integration and Testing Plan
- [RD8] TEC-FRA-DOC-2024-01143 - TCA Interface Control Document
- [RD9] TEC-FRA-DOC-2024-01015 - Huracan Trade-off Report


## TCA Overview

### Role of the TCA in the engine system

The primary function of the thrust chamber assembly is to provide thrust to the spacecraft. At the nominal operating point, the thrust chamber provides 15 kN of thrust in vacuum. The associated chamber pressure and mixture ratio are $30 bar$ and $3.4$ respectively. The thrust chamber is capable of throttling. The lowest thrust level is $50\%$ with growth potential to throttle between $33\%$ and $133\%$.

The thrust chamber assembly can be divided into four main components as we can see in Figure \ref{fig:tca} (in the TCA3 configuration with a long version of the NE). These are the injection head, combustion chamber, ignition system and nozzle extension. The thrust chamber assembly does not contain a thrust vector control system.

![Thrust chamber assembly\label{fig:tca}](definition_file_figures/tca.png)


### TCA Design Overview

In this section we give an overview of the main TCA components. For a detailed explanation and justification of the components please refer to [RD1].

#### Ignition System

The ignition system (Figure \ref{fig:wh_is}) is a high pressure torch that utilizes gaseous oxygen and gaseous methane, and its main purpose is to ignite the combustion chamber reliably and repeatedly. The choice of using a high pressure torch was mostly a consequence of its design simplicity and high power output. A full trade-off can be found in the Huracan Trade-off Report [RD9]. Figure \ref{fig:wh_is} shows the current design of the ignition system. This design is a battleship design meant to be used in the workhorse engine test campaign. It is not fully representative of the flight design, because it was designed to be very powerful and robust.

The power output of the igniter at this stage of development is rated at $365kW$. This power output is needed to ignite one third of the first row of injectors with a safety factor of $5$. The propellants are ignited using a spark plug, creating hot combustion gases at a nominal chamber pressure of $11 bar$. A spark plug is currently used for the development, but it does not mean it will be used for the flight design. Spark plugs can have unreliable performance in vacuum. A trade-off is currently open between spark plugs and glow plugs. This trade-off will be closed at the IGS & NE PDR.

The design consists of a double wall design, where the primary center flow has a mixture ratio of $12$. The secondary outer flow is entirely methane, and its purpose is to manage the thermal loads of the igniter. When we consider the secondary outer flow, the overall mixture ratio is brought down to $3$. In the primary flow, the oxygen is injected axially, and the methane is injected tangentially to create a swirling flow that protects the igniter wall and promote mixing. The igniter is operated for a maximum of $1.5$ seconds. The flame tube has a small convergent section to choke the flow and make it independent of the back pressure in the combustion chamber.

![Workhorse ignition system\label{fig:wh_is}](definition_file_figures/wh_ignition_system.png)

For a final flight ignition system, a few changes will be done. The actual power output required for successful ignition of the main chamber will be determined and scaling of the part will be done. This also includes a design which is optimized for additive manufacturing. This allows the ignition system and injector head to be potentially integrated together and printed as one. Due to the vacuum environment, a glow plug system will be more favorable and used going forward. The need for the secondary flow for cooling will also be refined through testing of the igniter. A more detailed explanation of the ignition system will be presented in the IGS & NE PDR at the end of Q1 2025.


#### Injection Head

The injection head, seen in Figure \ref{fig:ih_cut_view}, is responsible for injecting the propellants in the combustion chamber and for providing sufficient mixing. This is achieved with a combination of swirl and shear injectors. The injector pattern is composed by three injector rows arranged in a hexagonal pattern. The two innermost rows are swirl injectors, and the outermost row is composed of shear injectors. The total number of injectors is $37$ which translates to an element mass loading of $0.11kg/s$. Another important function of the injector head is to prevent combustion instabilities. A key design factor that has a large impact on the stability is the pressure drop of the injectors. At the nominal operating point, the oxygen injector pressure drop is $3bar$ and methane injector pressure drop is $4.5bar$ ($10\%$ and $15\%$ of the pressure drop respectively). At the $50%$ throttle condition, the oxygen injector pressure drop is $0.75bar$ and the methane injector pressure drop is $2.25bar$, which is $5\%$ and $15\%$ respectively, which satisfies the following requirement:

```yaml automation
config:
    processor: requirement
    configuration: reqs-huracan
    req_id: "t4_tca-415"
```

The injectors are balanced, i.e. they have the same mixture ratio and pressure drop between all elements. In order to ensure a homogenous propellant distribution, there are two distribution rings, one for each propellant, that distribute the propellants inside the propellant domes. This is needed because the propellant lines are attached radially to the injection head. The distribution rings have a thin plate that separate them from the propellant domes. These plates have small perforations with different sizes depending on the location.

By tailoring the size of the perforation to the local flow characteristics in the distribution ring we can guarantee a uniform distribution. The two main propellant inlets are separated by $180^{\circ}$ of each other for easier integration. The injector rows are not aligned with each other, but instead they have slight angular offsets to break symmetries. 

The cooling of the faceplate is achieved through a custom design lattice structure. The lattice structure increases the surface area available to exchange heat with the surrounding media. At the same time, it adds structural rigidity which enables the faceplate to be thinner.

This design is enabled by the additive manufacturing process. At the center of the injector head there is a hole for an axial ignition system.

![Cut view of injection head\label{fig:ih_cut_view}](definition_file_figures/injection_head_cut_view.png)

#### Combustion Chamber

The main combustion process occurs inside the combustion chamber. The thermal loads created by the combustion process are managed by using regenerative cooling in a counter flow configuration, see Figure \ref{fig:mcc_cut_view}.

The regenerative cooling starts at an expansion ratio of $12$. The propellant used in the regenerative circuit is methane. The cooling channels are constant in width, but they vary in height according to the local heat flux. The regions with the highest heat flux have smaller channels to increase the heat transfer on the cold side. In order to reduce the pressure drop in the channels, the cooling channels split upstream and downstream of the throat, which are areas with lower heat fluxes. This means that in the throat region the number of cooling channels is effectively reduced by half compared to the cylindrical and divergent sections.

The inner wall thickness is $0.5 mm$ and the smallest cooling channel ribs are $0.4 mm$. The propellant is fed to the cooling channels by a manifold at the end of the combustion chamber, and it is collected by another manifold at the other side of the cooling channels. The inlet manifold has a variable cross-section. The cross-section of the manifold reduces size the further it is from the inlet line. This creates a more homogenous distribution. The outlet manifold is constant in cross-section to avoid manufacturing deformations near the interface of the injector head and combustion chamber. Besides the regenerative cooling, there is also a Thermal Barrier Coating (TBC) made out of zirconium oxide. The TBC is $0.1 mm$ thick and covers the entire divergent section and part of the throat.

![Cut view of the combustion chamber with the regenerative circuit in red\label{fig:mcc_cut_view}](definition_file_figures/mcc_cut_view.png)

The cylindrical part of the combustion chamber has a length of $154 mm$, and the contraction ratio is $4$. This results in a characteristic length of $0.85 m$. 

The target combustion efficiency is $0.98$. The combustion products are expanded through a convergent divergent nozzle, whose contour is a parabolic nozzle that follows Rao’s guidelines; also called Thrust Optimized Parabola (TOP). This means that the convergent throat radius and the divergent throat radius are defined by a certain constant, which are $1.5$ for both. These constants are multiplied by the throat radius to obtain the curvature radius.

The throat diameter is $56.2mm$. The contour of the combustion chamber can be seen in Figure \ref{fig:mcc_profile}. The target efficiency of the thrust chamber assembly is $365s$ of ISP. The combustion chamber stops at an expansion ratio of $12$. After that point, the expansion is continued by the nozzle extension.

![Combustion chamber profile\label{fig:mcc_profile}](definition_file_figures/combustion_chamber_profile.png)

The nozzle extension part is a large portion of the nozzle that continues the expansion process that was initiated in the combustion chamber. The objective of the nozzle extension is to convert as much thermal energy from the combustion gases in kinetic energy (thrust of engine). Also, the outlet pressure of the nozzle extension shall closely match the ambient pressure. In case of a vacuum engine like Huracan, a trade-off between a longer nozzle to convert more energy and additional mass of the component is made.

The igniter, injection head and combustion chamber are all manufactured with Laser Powder Bed Fusion (LPBF). The material for all of these components is Inconel 718, which was chosen for its high corrosion resistance and high strength at elevated temperatures.

#### Nozzle Extension

The trade-off of the material of the nozzle extension is still ongoing. In this section we present the current baseline for the NE which is a metallic nozzle made from the high-temperature alloy Haynes 282 and manufactured using Direct Energy Deposition (DED). The main method of cooling for the nozzle extension is radiation cooling, however at the beginning of the nozzle extension the thermal loads are too high. For this reason, film cooling is used to supplement the radiation cooling. The film cooling uses $5\%$ of the overall methane mass flow (i.e. $5\%$ of $1 kg/s$). At the nominal operating point, the methane supply for the film cooling is 180K at $1.1 bar$. The film cooling helps to reduce the wall temperature, but it comes at the cost of performance. With this amount of film cooling, it is estimated that there will be a $5/%$ loss of ISP. Nevertheless, we can accept this reduction in performance, because it is still within the $10s$ os ISP loss that we can accept. 

The supply of this methane mass flow is yet to be decided. A part could come from the leakage passage in the methane pump motor around the dynamic seal. As an opportunity, instead of trying to have a perfect dynamic seal at the pump’s high-speed shaft, this intentional leak is captured and discharged via the nozzle cooling. This possibility should be further investigated during the concept of the in-house Fuel Pump design.

The final trade-off and flight design will be presented on the IGS & NE PDR at the end of Q1 2025. There a flight like design will be presented along with the justification of the design. In Figure \ref{fig:ne_fig} we see a very preliminary design of the NE. The major difference from this design to the flight-like design will be the interface with the MCC.

![Nozzle Extension preliminary design (color not representative of material)\label{fig:ne_fig}](definition_file_figures/ne_fig.png){width=60%}

#### Geometric characterisitcs

Key geometric characteristics of the thrust chamber assembly are listed below:

- Main components:
    - Injection head
        - 3.2 mm LOX post diameter
        - 0.4mm LOX post wall 
        - 0.6mm methane annulus gap
        - 37 injectors arranged in 3 rows
        - Height of 65mm
    - Combustion chamber
        - 56 mm throat diameter
        - 4 contraction ratio
        - 12 expansion ratio at combustion chamber exit
        - 0.5mm inner wall thickness
        - Length of 366mm
    - Ignition system
        - 10 mm tube diameter
        - 1 mm tube wall thickness
        - 1 mm cooling annulus width 
        - 8.1 mm throat diameter
        - 8.85 contraction ratio
    - Nozzle extension
        - 125 expansion ratios
        - 630mm exit diameter
        - 197 mm inlet diameter
        - 728 mm length
    - Cylindrical envelope
        - 1160 mm length
        - 628 mm diameter 
    - In- and outlet
        - AS5202-12 boss ports

#### PBS mass budget

In Figure \ref{fig:tca_pbs} we can see the comparison between the target weight and the actual weight for each component on the TCA. It is clear that all components are above the target weight at this stage of the development. It is important to note that the weight of the parts is taken from the development models and not the final flight design. Some components, like the ignition system and the nozzle extension, are still in a very preliminary design phase. Additionally, some targets might not be realistic, since they were defined very early in the project. For example, the mass target for the NE considers a composite nozzle. If a metallic nozzle extension is chosen, the mass target will never be reached. The MCC and IH are closer to a flight-like design, but still implement interfaces meant for development. Changing the interfaces to welded connections or combining the different parts into one print are some options that can be considered to remove weight. In the TCA Development Plan [RD2] a detailed weight reduction plan is provided.

![Thrust Chamber Assembly – PBS - Mass budget\label{fig:tca_pbs}](definition_file_figures/tca_pbs.png){width=40%}


#### State of development

The IH and MCC have completed the preliminary design phase. This phase included:

- swirl injector single element tests in ambient and vacuum
- TCA1 water cooled campaign
- TCA2 methane cooled campaign
- IH & MCC PDR

In order to provide the complete overview of the current status, we provide as support documents the test reports of previously mentioned test campaigns ([RD4-6]). In short, it was observed that the pressure drop of the injectors is close to the target one and that the combustion efficiency meets the requirements when we use gaseous methane. However, it was also observed that the outlet temperature of the RC is much lower than expected and when fed directly to the IH, it reduces the combustion efficiency significantly. 

The next step for these components is the TCA3 test campaign (in November and December of 2024) that will study reduction of TBC, sub- and supercritical methane cooling and variable fuel injection temperature. Following this campaign, the parts will be redesigned ahead of the DM1 with a special focus on matching the injector design to the RC outlet in order to recover the high combustion efficiency. For a complete overview of the development plan and test plan please refer to [RD2] and [RD3].

On the other hand, the IGS and the NE are still in a preliminary design phase and have open trade-offs. Preliminary designs of these components will be tested during the TCA3 test campaign. These tests will help close the trade-off. The ignition system will also undergo standalone tests in order to narrow down the power requirements. Both components will have a PDR in Q1 of 2025, where the major trade-offs will be closed and flight-like designs will be presented.


### Working Principles

#### Thrust generation

The working principle of the thrust chamber assembly is based on the Newton's third law of motion that states that for every action there is an equal and opposite reaction. In this case, the TCA expels very fast moving gases through a nozzle which creates a force in the other direction. In order to increase the amount of thrust, a rocket engine can either expel more mass, or expel the same mass at a greater velocity. To achieve the latter, the propellants must undergo a series of different process to convert their chemical potential energy into kinetic energy. The most important processes are mixing, combustion and expansion.

When the propellants arrive in the TCA, they are at high pressure and separated from each other. For an efficient combustion it is important that the propellants are properly mixed. For this purpose, the propellants are injected through many injector elements composed by small orifices. The objective of the injectors is to force the propellants to interact with each other and achieve an homogenous mixture. There are many injectors geometries and each one is better suited for a specific application and propellant combination. The Huracan TCA uses coaxial injectors that inject the propellants at very different velocities. This creates Kelvin Helmholtz instabilities through the action of intense shear forces. These instabilities create strong vortices that thoroughly mix the propellants.

For most propellants, an external energy source is required to start the combustion process. This energy source needs to be high enough to raise the temperature of the propellants above their auto-ignition temperature. In order to achieve reliable and repeatable ignition in vacuum, a smaller combustion chamber is used. The propellants in this small combustion chamber are ignited using a spark plug that is excited by a 24V energy supply. The spark plug generates high temperature plasma that starts the reaction. Then the products from this small combustion chamber enter the main combustion chamber which ignite the propellants.

Once the reaction process has started, the propellants continue to react as long as fresh propellant is injected in the combustion chamber. This is due to the fact that during the reaction process large amounts of energy are released in the form of heat which is capable to self sustain the reaction. This heat release turns the propellants into high pressure and high temperature gases. It is the objective of the combustion chamber to contain these gases and directed them through a nozzle where they are free to expand.

The purpose of the expansion process is to convert the thermal energy of the propellants into the kinetic energy. This is achieved by using a convergent divergent nozzle. A convergent divergent nozzle is a type of nozzle that has a constriction known as the throat. Until the throat, the flow accelerates until it reaches the speed of sound. After the throat the flow continues to expand in the divergent part, reaching supersonic velocities. Flows in the supersonic regime can have complex phenomena such as shocks that decrease the efficiency of the expansion process. Additionally, if the exhaust velocity has velocity components perpendicular to the nozzle axis this will also lead to losses. The shape of the nozzle needs to minimize all of these loses by trying to expand the flow in a shock free condition until the pressure of the gases reaches the pressure outside the nozzle. Sometimes this is not possible due to size and weight restrictions. All the force produced by the nozzle needs to be transferred to the vehicle. This means that the structure of the TCA not only needs to withstand the pressure of the propellants but also needs to be able to carry this load. 

#### Thermal management

As mentioned before the combustion process releases a huge amount of energy. For a methalox engine the temperature of the combustion gases can be anywhere between $3,000$ to $3,500 K$ which is higher than the melting temperature of most metals. Therefore, it is essential to manage the temperature of the structure to ensure that it does not lose its structural integrity. 

There are different methods of cooling depending on the application. For larger engines the most common method is regenerative cooling, where usually one propellant (commonly the fuel) flows through narrow channels that are in contact with the inner wall of the combustion chamber. The heat is transferred from the combustion gases through the wall of the chamber and into the fuel. Not only does this cool the wall, but it also raises the enthalpy of the propellant which improves the combustion process. 

Sometimes regenerative cooling is not sufficient, and it needs to be used in combination with other methods. For example, the combustion chamber wall can be coated with a ceramic, typically made from yttria stabilized zirconia, which has a very high melting temperature and a very low thermal conductivity, which reduces the heat load from the combustion gases to the combustion wall. 

It is important to note that regenerative cooling also brings some disadvantages to the system. In order to achieve efficient cooling, it is necessary to have high velocities in the cooling channels, which in turn increase the pressure drop and raise the pressure requirements for the pumps. This restricts the use of this cooling technique to areas with high thermal loads where other cooling techniques would not be sufficient, like the areas close to the throat. As the flow expands and moves away from the throat, the temperature of the combustion gases decreases and other cooling techniques become more viable. One of them is radiative cooling, which uses the fact that all materials emit thermal radiation to cool the wall of the nozzle. For this process to be efficient it is important to use materials with high emissivity properties. In areas where radiative cooling is still not enough, it can be complemented with film cooling, where a small amount of propellant is injected close to the walls of the nozzle. The injected propellant also acts as a thermal barrier and protects the wall form the combustion gases. 

The Huracan TCA uses all the aforementioned techniques. The combustion chamber uses regenerative cooling and thermal barrier coatings due to the high heat fluxes. Then the nozzle extension is cooled using film cooling for the first few centimeters and the rest is cooled through radiative cooling.

## Functional Characteristics

### Limitations and operating domain

The TCA is meant to operate in a range of $100\%$ to $50\%$ thrust. Two parameters are regulated to throttle the engine within this range, namely the combustion chamber pressure $P_{CC}$ and the mixture ratio $MR$. As one can notice, the mixture ratio is held constant.  
The combustion pressure being relatively low, the critical point of methane lies above the chamber pressure. This means that subcritical conditions may occur upstream in the fuel line. The performance of subcritical methane in the regenerative circuit was not fully characterized yet and will be further assessed in test campaigns. Therefore, an additional limitation $P_{FCO}$ was added to keep the pressure in the regenerative circuit in supercritical condition. This worst case scenario constraint is the current baseline but could be relaxed according to coming test results.  
Notice that the mass flow at the regenerative circuit inlet $M_{FCI}$ is generally larger than the mass flow through the fuel injector $M_{FII}$. Indeed, a certain proportion of the fuel mass flow is tapped off downstream the regenerative circuit to feed a pressurization buffer.

A summary table of the limitations is shown below: 

|                       | 100%      |50%        |
|-----------------------|:---------:|:---------:|
|$P_{CC}$               | 30 bar    | 15 bar    |
|$MR$                  | 3.4       | 3.4       |
|$P_{FCO}$              | >48 bar   | >48 bar   |

The conditions in both maximum and minimum throttle were computed[^note] in steady state and the most relevant values are described in the Figures \ref{fig:ecosim_ref_100_TCA} and \ref{fig:ecosim_ref_50_TCA}.

![Reference 100% thrust, main TCA values from Ecosim\label{fig:ecosim_ref_100_TCA}](definition_file_figures/Ecosim_TCA_std_100.png){width=70%}

![Reference 50% thrust, main TCA values from Ecosim\label{fig:ecosim_ref_50_TCA}](definition_file_figures/Ecosim_TCA_std_50.png){width=70%}

On another note, the computed engine thrust is slightly greater than target (15.1 kN for the 100% thrust point and 7.6 kN for the 50% thrust point). This comes from the fact that the Main Combustion Chamber (MCC) has been sized without taking into consideration the additional contribution to Nozzle Extension film cooling to the overall engine thrust. The computation made in Ecosim uses the current version of Nozzle Extension which uses film cooling as a baseline. It is however not frozen yet and may still change. This point is not of concern as the chamber pressure will be adapted to get back to the specified values. Adapting the MCC design later in the development when the overall system is further characterized (presence of Thermal Barrier Coating or not, refined estimation of the film cooling contribution to thrust…) will not require a lot of effort and is also to be considered.

[^note]:
    all the steady results that are presented in this section (Functional characteristics) have been obtained using the EcosimPro software. The models used have been built in-house.

### Operating conditions
<!--@PierreMorinTEC-->

The reference operating points were specified in the previous section. However, due to unknowns and inherent scattering from each component of the system, the engine might experience a deviation from this reference. In order to identify the flight domain in which the system has most chances to operate, a dedicated scattering study was performed. While scattering factors were applied to the whole engine system, the impact is observed at sub-system level. 

To ease the reading of the scattering functional domain charts, below is given a list of notes: 

- Each point represents a scattered engine. The sources for this scattering are unknowns, which shall be driven to zero as the product is matured, and inherent scattering due to manufacturing tolerances, measurement errors… 
- 20,000 scattered engines are simulated in order to define the functional domains 
- The functional domains are depicted as red contours and defined considering a probability of 99%. This means that a component has 99% of chance to operate within the defined functional domain. 
- 4 points (Q1, Q2, Q3, Q4) are eventually shown. Those are the qualification points which shall be defined in order to allow to qualify as good as possible each subsystem. The 4 qualification points are presented at TCA level in Figures \ref{fig:ecosim_Q1_TCA}, \ref{fig:ecosim_Q2_TCA}, \ref{fig:ecosim_Q3_TCA}, \ref{fig:ecosim_Q4_TCA}
- 4 flight domains are shown. _Close Loop 100%_, _Close loop 75%_, _Close Loop 50%_ correspond to the scattered engines in closed loop and given throttle condition. _Close Loop 50% w/o pres_ correspond to the scattered engines at 50% throttling level and with the pressurization by-pass flow set to zero. Turning off the pressurization mass flow at low throttle level is an option currently being considered and is thus depicted in the functional domains.
- "STEADY_OK" means that only the successful simulations are taken into account. Nevertheless, the simulation success rate is very high (>99.9%) and thus almost all scattered engines are taken into account.

![Qualification point Q1, main TCA values from Ecosim\label{fig:ecosim_Q1_TCA}](definition_file_figures/Q1_TCA.png){width=70%}

![Qualification point Q2, main TCA values from Ecosim\label{fig:ecosim_Q2_TCA}](definition_file_figures/Q2_TCA.png){width=70%}

![Qualification point Q3, main TCA values from Ecosim\label{fig:ecosim_Q3_TCA}](definition_file_figures/Q3_TCA.png){width=70%}

![Qualification point Q4, main TCA values from Ecosim\label{fig:ecosim_Q4_TCA}](definition_file_figures/Q4_TCA.png){width=70%}

The operating conditions in the plane of the regulated parameters, $P_{CC}$ and $MR$ is shown in Figure \ref{fig:mrc_pcc_Qpoints}. The flight domain spans over a mixture ratio $MR \in [3.26, 3.54]$ and a chamber pressure $P_{CC} \in [14.6, 30.9]$ bar.


![Flight domain and qualification points in the MR-PCC plane\label{fig:mrc_pcc_Qpoints}](definition_file_figures/MRC-PCC-Qpoints.png)

#### Temperature range

The reference inlet temperature at different throttling level as well as the expected range is presented in the following table and figures. 

|                           | 100%      | 50%       |
|---------------------------|:---------:|:---------:|
| **LOX IH inlet reference**    | **93.3 K**    | **94.6 K**    |
| LOX IH inlet max          | 99.2 K    | 101 K     |
| LOX IH inlet min          | 91.5 K    | 90.7 K    |
| **LCH4 RC inlet reference**   | **117.2 K**   | **117.8 K**   |
| LCH4 RC inlet max         | 123.5 K   | 124.5 K   |
| LCH4 RC inlet min         | 112.8 K   | 113.4 K   |

![LOX injector head inlet temperature range\label{fig:PCC_vs_TOII}](definition_file_figures/PCC_TOII.png)

![LCH4 regenerative circuit inlet temperature range\label{fig:PCC_vs_TFCI}](definition_file_figures/PCC_TFCI.png)

In Figure \ref{fig:rc_pdr_t_out} we can see the regenerative circuit outlet temperature of the methane and in Figure \ref{fig:rc_pdr_wall_temp} we see the maximum wall temperature of the combustion chamber. Note that these figures are the result of the numerical simulations of the current prototype (TCA3) and are calibrated to the results of the previous test campaign (TCA2 methane cooled campaign). This means that these results are not necessarily the same ones as the final flight design. For more information on the numerical model please refer to TCA Justification File [RD1].

![Methane regenerative circuit outlet temperature, $T_{in}=115K$, $P_{in}=55bar$\label{fig:rc_pdr_t_out}](definition_file_figures/rc_pdr_t_out.png){width=60%}

![Main combustion chamber maximum wall temperature, $T_{in}=115K$, $P_{in}=55bar$\label{fig:rc_pdr_wall_temp}](definition_file_figures/rc_pdr_wall_temp.png){width=60%}


#### Pressure range

The reference inlet pressures at different throttling level as well as the expected range is presented in the following table and figures. 

|                           | 100%        | 50%         |
|---------------------------|:-----------:|:-----------:|
| **LOX IH inlet reference**    | **33.0 bar**    | **15.8 bar**    |
| LOX IH inlet max          | 34.9 bar    | 16.26 bar     |
| LOX IH inlet min          | 31.9 bar    | 15.48 bar    |
| **LCH4 RC inlet reference**   | **54.0 bar**    | **50.4 bar**    |
| LCH4 RC inlet max         | 56.6 bar    | 52.14 bar    |
| LCH4 RC inlet min         | 51.4 bar    | 48.74 bar    |

![LOX injector head inlet pressure range\label{fig:PCC_vs_POII}](definition_file_figures/PCC_POII.png)

![LCH4 regenerative circuit inlet pressure range\label{fig:PCC_vs_PFCI}](definition_file_figures/PCC_PFCI.png)

In Figure \ref{fig:rc_pdr_dp} we can see the regenerative circuit pressure drop for the current TCA3 design. 

![Regenerative circuit pressure drop, $T_{in}=115K$, $P_{in}=55bar$\label{fig:rc_pdr_dp}](definition_file_figures/rc_pdr_dp.png){width=60%}

 In Figure \ref{fig:rc_tca_pdr_lox} and \ref{fig:rc_tca_pdr_fu} we can see the injectors' pressure drop and the respective dome pressure. Note that these figures are the result of the numerical simulations of the current prototype (TCA3) and are calibrated to the results of the previous test campaign (TCA2 methane cooled campaign). On the LOX side, we see that the pressure drop at the nominal point is exactly the same one as the reference, but on the fuel side, it is slighly lower. This is due to the low methane regenerative circuit outlet temperature of the current design. The future iterations will have slight design modifications to bring the pressure drop back to the reference level. For more information on the injectors please refer to TCA Justification File [RD1].

![LOX injectors pressure drop (left) and LOX dome pressure (right)\label{fig:rc_tca_pdr_lox}](definition_file_figures/rc_tca_pdr_lox.png){width=110%}

![Fuel injectors pressure drop (left) and fuel dome pressure (right)\label{fig:rc_tca_pdr_fu}](definition_file_figures/rc_tca_pdr_fu.png){width=110%}

#### Mixture ratio (mass flows)

The reference inlet mass flows at different throttling level as well as the expected range is presented in the following table and figures. Note that a third column was added accounting for the case when the heat exchanger is turned off. This may happen at low thrust when the pressurization could be stopped.

|                           | 100%          | 50%           | 50% w/o pres. |
|---------------------------|:-------------:|:-------------:|:--------------|
| **LOX IH inlet reference**    | **3.24 kg/s**     | **1.63 kg/s**     | **1.63 kg/s** |
| LOX IH inlet max          | 3.35 kg/s     | 1.69 kg/s     | 1.69 kg/s     |
| LOX IH inlet min          | 3.12 kg/s     | 1.57 kg/s     | 1.57 kg/s     |
| **LCH4 RC inlet reference**   | **1.00 kg/s**     | **0.50 kg/s**     | **0.48 kg/s** |
| LCH4 RC inlet max         | 1.08 kg/s     | 0.54 kg/s     | 0.50 kg/s     |
| LCH4 RC inlet min         | 0.93 kg/s     | 0.46 kg/s     | 0.46 kg/s     |
| **Combustion MR reference**      | **3.40**   | **3.40**  | **3.40** |
| MR max                   | 3.55          | 3.54          | 3.54          |
| MR min                   | 3.26          | 3.26          | 3.26          |

![LOX injector head inlet mass flow range\label{fig:PCC_vs_MOII}](definition_file_figures/PCC_MOII.png)

![LCH4 regenerative circuit inlet mass flow range\label{fig:PCC_vs_MFCI}](definition_file_figures/PCC_MFCI.png)


### Thrust 

The reference thrust in vacuum at different throttling level as well as the expected range is presented in the following table and figures. As previously mentioned, the difference in reference thrust arises from whether or not film cooling is considered.

|                           | 100%        | 50%         |
|---------------------------|:-----------:|:-----------:|
| **Thrust in vacuum reference**    | **15.1 kN**    | **7.6 kN**    |
| Thrust in vacuum max              | 15.84 kN    | 7.97 kN     |
| Thrust in vacuum min              | 14.39 kN    | 7.24 kN    |

![LOX injector head inlet pressure range\label{fig:PCC_vs_THRUST_VAC}](definition_file_figures/PCC_THRUST_VAC.png)

### ISP


The reference specific impulse in vacuum at different throttling level as well as the expected range is presented in the following table and figures. The Isp calculated in this section refers to the one at TCA level. It does not take the reduction of specific impulse due to the mass flow tapped off for pressurization. In addition, note that it takes into account the contribution of film cooling.

|                           | 100%        | 50%         |
|---------------------------|:-----------:|:-----------:|
| **Isp in vacuum reference**    | **363.6 s**    | **359.7 s**    |
| Isp in vacuum max              | 379.3 s    | 375.0 s     |
| Isp in vacuum min              | 348.0 s    | 344.5 s    |

![LOX injector head inlet pressure range\label{fig:PCC_vs_ISPCC_VAC}](definition_file_figures/PCC_ISPCC_VAC.png)

### Transients

The TCA is able to operate the following transients:

- 0% to 90% thrust: max 2.5 seconds (start-up)
- 100% to 0% thrust: max 2.5 seconds (shut-down)

These values were deduced from the TCA2 test campaign. The start-up and shutdown sequences were regulated and after optimization, they would likely allow faster transients. For illustration, a typical start-up and shut-down sequence from TCA2 is shown in Figures \ref{fig:startup_TCA2} and \ref{fig:shutdown_TCA2}.

![Typical start-up phase during TCA2 campaign\label{fig:startup_TCA2}](definition_file_figures/typical_startup_TCA2.png){width=50%}

![Typical shut-down phase during TCA2 campaign\label{fig:shutdown_TCA2}](definition_file_figures/typical_shutdown_TCA2.png){width=50%}

## Mechanical Characteristics 

### List of Materials and Processes

Described in the MAIT Plan [RD7].

### Description of connections and interfaces

Described in the ICD [RD8].

### Mechanical margin

The mechanical margin is explained in the TCA Justification File in a dedicated "Mechanical" section [RD1]. Inside this section, the TCA margin policy is also defined.


## Conclusion

The TCA Definition File provides an overview of the TCA's design, performance characteristics and mechanical properties.

- The IH and MCC were designed iteratively with a strong focus on rapid iterations and high test cadence.
- The IGS and NE are still in a preliminary design phase.
- The MCC is regenerative cooled with the help of TBC. The NE is radiation cooled with the help of film cooling if a metallic nozzle is used.
- Extensive mechanical analysis has been used to validate the mechanical integrity of the TCA.
- The selection of the materials and processes for the TCA are strongly driven by the short iteration cycles

The IH and MCC design already have a mature design. Currently, the focus is on achieving high combustion efficiency by doing minor modifications on the injectors and the cooling circuit of the MCC. The IGS and NE are still in a preliminary design phase and the PDR for these components will be held in Q1 of 2025.
