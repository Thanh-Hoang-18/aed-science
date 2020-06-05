---
title: "AED2/AED2+ Manual"
author: ""
date: "2020-05-24"
site: bookdown::bookdown_site
documentclass: book
bibliography:  ["references/pathogens.bib",
              "references/generic_utilities_functions.bib",
              "references/bivalves.bib"]
biblio-style: apalike
link-citations: yes
github-repo: AquaticEcoDynamics/aed-science
url: ''
description: "Work in progress."
---

<!--chapter:end:index.Rmd-->


# Welcome{-}

Welcome!

\BeginKnitrBlock{rmdcaution}<div class="rmdcaution">This is a note! A small graphic icon can be inserted next to the text too. </div>\EndKnitrBlock{rmdcaution}

This is a map[^1]!

<center>
<!--html_preserve--><div id="htmlwidget-1a813d19350a10492c91" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-1a813d19350a10492c91">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"setView":[[-32.835,116.037],10,[]],"calls":[{"method":"addTiles","args":["//{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap<\/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA<\/a>"}]},{"method":"addMarkers","args":[-32.835,116.037,null,null,null,{"interactive":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},"buried treasure here",null,null,null,null,{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]}],"limits":{"lat":[-32.835,-32.835],"lng":[116.037,116.037]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->
</center>

## How to contribute?{-}

## Reproducibility{-}

## Supporting the project{-}

[^1]: Here is a footnote.

<!--chapter:end:01-welcome.Rmd-->

# Foreward{-}


<!--chapter:end:02-foreward.Rmd-->

# Preface{-}


<!--chapter:end:03-preface.Rmd-->

# Introduction

## Scientific Overview


## Application Contexts


## Book Structure











<!--chapter:end:04-intro.Rmd-->

# Nomenclature

## A Note on Notation

The remainder of this section presents the range of equations and parameterisations adopted by the various model approaches. For consistency, a standard mathematical notation is used.

- $N$ = number of groups (integer)
- $a, om, z$ = indices of various sub-groups of algae/phytoplankton, organic matter and zooplankton (integer)
- $\chi_{C:Y}^{group}$ = the stoichiometric ratio of “$group$” between $C$ and element “$Y$”  (mmol C/mmol Y)
- $f_{process}^{var}$ = function that returns the mass flux of “$process$” on “$var$”  (mmol var/time)
- $R_{process}^{var}$ = the rate of “$process$” influencing the variable “$var$”  (/time)
- $F_{process}^{var}$ = the maximum benthic areal flux of variable “var” (mmol var/area/time)
- $p_{source}^{group}$ = the preference of “$group$” for “$source$”  (0-1)
- $\Phi_{lim}^{group}(var)$ = dimensionless limitation or scaling function to account for the effect of “$lim$” on “$group$” (-)
- $k^{var}$	= generic fraction related to “$var$”  (0-1)
- $\Theta_{config}^{group}$	= switch to configure selectable model component “$config$” for “$group$” (0,1,2,…)
- $c,\theta,\gamma…$ 		= coefficient  (various units)


## Data Types

<!--chapter:end:05-nomenclature.Rmd-->

# Organisation of the Library & Module Structure

## Library Design


## Model Structure
<!-- Previously from 'Modelling within the AED framework'-->

The AED2 Model has ability to simulate a range of physical, chemical and biological processes, that can be generally described based as:

-	Feedback of chemical or biological attributes to physical properties of water (light extinction, drag, density)
-	Water column kinetic (time-varying) chemical / biological transformations (e.g., denitrification or algal growth)
-	Water column equilibrium (instantaneous) chemical transformations (e.g., PO~4~ adsorption)
-	Biogeochemical transformations in the sediment or biological changes in the benthos
-	Vertical sedimentation or migration
-	Fluxes across the air-water interface
-	Fluxes across the sediment-water interface
-	Fluxes across the terrestrial-water interface (riparian interactions)
-	Ecohydrological dynamics and biogeochemical transformations in the exposed (dry) cells
-	Feedbacks of soil and vegetation dynamics onto lake hydrodynamics and water balance

The model is organised as a series of “modules” that can be connected or “linked” through specific variable dependencies. Relevant variables (Table 3) are described in the following sections, along with the science basis relevant to the Lower Lakes model setup. For the initial phase of the CLLMM RWQM model, only the core variables are configured, and future proposed variables are also indicated in the Table 3, denoted with an asterisk.

## Module Summary

<!--chapter:end:06-organisation_and_structure.Rmd-->

# Coupling to Host Models

## Interface Approach


## “Environment” Variables


## Feedback Options


## Light Climate


## Velocity & Stress


## Sediment Zones


## Lagrangian Particles


## Current Hosts


<!--chapter:end:07-host_model_coupling.Rmd-->

# (PART)  AED Water Modules{-} 

# Tracers & Water Age

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:08-tracers_water_age.Rmd-->

# Suspended Sediment

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:09-suspended_sediment.Rmd-->

# Dissolved Oxygen 

## Contributors


## Overview 

Dissolved Oxygen (DO) dynamics respond to processes of atmospheric exchange, sediment oxygen demand, microbial use during organic matter mineralisation and nitrification, photosynthetic oxygen production and respiratory oxygen consumption, chemical oxygen demand, and respiration by other biotic components such as seagrass and bivalves (see table below).

Other processes impacting the oxygen concentration include the breakdown of DOC by aerobic heterotrophic bacteria to CO2, whereby a stoichiometrically equivalent amount of oxygen is removed. Chemical oxidation, for example processes such as nitrification or sulfide oxidation, also consume oxygen dependent on the relevant stoichiometric factor. Photosynthetic oxygen production and respiratory oxygen consumption by pelagic phytoplankton is also included and is summed over the number of simulated phytoplankton groups. Seagrass interaction with the oxygen cycle is configurable within the model.


## Model Description

### Process Descriptions

<!-- previously from 'aed2_oxygen : oxygen solubility & atmospheric exchange' on website version-->
#### Oxygen Solubility & Atmospheric Exchange {-} 
Atmospheric exchange is typically modelled based on Wanninkhof (1992) and the flux equation of Riley and Skirrow (1974) for the open water, and on Ho et al. (2011) for estuarine environments.
\begin{equation}
								F_{O_2} = k_{O_2} \left(C_{air} - C_{water}\right)
\end{equation}
Where $k_{O_2} (ms^{-1})$ is the oxygen transfer coefficient, $C_{water} (gm^{-3})$ is the oxygen concentration in the surface waters near the interface and $C_{air} (gm^{-3})$ is the concentration of oxygen in the air phase near the interface. A positive flux represents input of oxygen from the atmosphere to the water. $C_{air}$ is dependent on temperature, $T$, salinity, $S$ and atmospheric pressure, $p$, as given by:
\begin{eqnarray}
							C_{air}\left(T,S,p \right) &=& 1.42763\: f\left(p\right) \exp \left\{ -173.4292+249.6339 \left[\frac{100}{\theta_k}\right] + 143.3483 \ln \left[ \frac{\theta_k}{100}\right] \right. \nonumber \\ &-& \left. 21.8492 \left[\frac{\theta_k}{100}\right] + S\left(-0.033096 +0.014259 \left[\frac{\theta_k}{100}\right] -0.0017 \left[\frac{\theta_k}{100}\right]^2 \right) \right\}
\end{eqnarray}
Where $\theta_k$ is temperature in degrees Kelvin, salinity is expressed as parts per thousand and atmospheric pressure is in kPa. The pressure correction function, $f(p)$ varies between one and zero for the surface and high altitudes respectively: 
\begin{equation}
							f\left(p\right)=\frac{p_H}{p_{SL}}\left[1-\frac{p_{vap}}{p_H}\right]/\left[1-\frac{p_{vap}}{p_{SL}}\right].
\end{equation}


#### aed2_oxygen : sediment oxygen demand {-} 
Modelling sediment oxygen demand can take a variety of forms. The simplest form in AED2 is the $SOD$ varies as a function of the overlying water temperature and dissolved oxygen levels.
\begin{equation}
							f_{O_2}^{DSF}(T,DO)= S_{SOD}\:f_{SED}^{T2}(T)\:f_{SOD}^{DO1}(DO)
\end{equation}

Where $S_{SOD}$ is a fixed oxygen flux across the sediment-water interface and $K_{DO_{SOD}}$ is a half-saturation constant for the sediment oxygen demand.

#### Other oxygen sources/sinks (optional) {-} 
- Oxygen consumption during baterial mineralisation of DOC is done in the bacteria module - aed2_bacteria;
- Oxygen consumption during nitrification is done in the nitrogen module - [aed2_nitrogen][Inorganic Nutrients: C/N/P/Si];
- Oxygen production/consumption by phytoplankton phtosynthesis/respiration is done in the phytoplankton module - [aed2_phytoplankton][Phytoplankton];
- Oxygen consumption due to zooplankton respiration is done in the zooplankton module - [aed2_zooplankton][Zooplankton];
- Oxygen production/consumption by seagrass phtosynthesis/respiration is done in the bateria module - aed2_seagrass;
- Oxygen consumption due to bivalve respiration is done in the benthic module - [aed2_benthic][Benthic Vegetation];

### Variable Summary

<table>
<tr>
<td> Variable Name </td> <td> Description </td> <td> Units </td> <td> Variable Type </td> <td> Core/Optional </td> 
</tr>
<tr>
<td>
```
OXY_oxy
```
</td>
<td>
Dissolved oxygen concentration
</td>
<td>
$mmol\,m^{-3}$
</td>
<td>
Pelagic
</td>
<td>
Core
</td>
</tr>
</table>

#### Diagnostics{-}
<table>
<tr>
<td> Variable Name </td> <td> Description </td> <td> Units </td> <td> Variable Type </td> <td> Core/Optional </td> 
</tr>

<tr>
<td>
```
OXY_oxysat
```
</td>
<td>
Dissolved oxygen saturation
</td>
<td>
%
</td>
<td>
Pelagic diagnostic
</td>
<td>
Core
</td>
</tr>

<tr>
<td>
```
OXY_atm_oxy_flux
```
</td>
<td>
O2 exchange across atm/water interface
</td>
<td>
$mmol\,m^{-2}\,day^{-1}$
</td>
<td>
$-$
</td>
<td>
$-$
</td>
</tr>

</table>

<!-- Previously from 'Parameters & Configuration' on website-->
<table>
<tr>
<td> Parameter Name </td> <td> Description </td> <td> Units </td> <td> Parameter Type </td> <td> Default </td> <td> Typical Range </td> <td> Comment </td> 
</tr>

<tr>
<td>
```
oxy_initial
```
</td>
<td>
Initial dissolved oxygen (DO) concentration
</td>
<td>
$mmol\,m^{-3}$
</td>
<td>
Float
</td>
<td>
$-$
</td>
<td>
0-400
</td>
<td>
Note: will be overwritten by GLM or TFV IC
</td>
</tr>

<tr>
<td>
```
Fsed_oxy
```
</td>
<td>
Sediment oxygen demand (SOD)
</td>
<td>
$mmol\,m^{-2}\,day^{-1}$
</td>
<td>
Float
</td>
<td>
$-$
</td>
<td>
-100
</td>
<td>
Note: unused if Fsed_oxy_variable is activated via aed2_sedflux
</td>
</tr>

<tr>
<td>
```
Ksed_oxy
```
</td>
<td>
Half-saturation concentration of oxygen sediment flux
</td>
<td>
$mmol\,m^{-3}$
</td>
<td>
Float
</td>
<td>
50
</td>
<td>
10-100
</td>
<td>
Changes the sensitivity of the oxygen flux to the overlying oxygen concentration
</td>
</tr>

<tr>
<td>
```
theta_sed_oxy
```
</td>
<td>
Arrhenius temperature multiplier for sediment oxygen flux
</td>
<td>
$-$
</td>
<td>
Float
</td>
<td>
1e+00
</td>
<td>
1.04 - 1.12
</td>
<td>
Changes the sensitivity of the oxygen flux to the overlying temperature
</td>
</tr>

<tr>
<td>
```
Fsed_oxy_variable
```
</td>
<td>
Oxygen sediment flux variable link
</td>
<td>
$-$
</td>
<td>
String
</td>
<td>
$-$
</td>
<td>
e.g.: SDF_Fsed_oxy
</td>
<td>
Will use the value supplied by the aed2_sedflux model for Fsed_oxy; use this option to allow for spatial or temperal variation
</td>
</tr>

<tr>
<td>
```
oxy_min
```
</td>
<td>
Minimum dissolved oxygen (DO) concentration
</td>
<td>
$mmol\,m^{-3}$
</td>
<td>
Float
</td>
<td>
$-$
</td>
<td>
$-$
</td>
<td>
Optional variable to enforce negative number clipping
</td>
</tr>

<tr>
<td>
```
oxy_max
```
</td>
<td>
Maximum dissolved oxygen (DO) concentration
</td>
<td>
$mmol\,m^{-3}$
</td>
<td>
Float
</td>
<td>
$-$
</td>
<td>
1000
</td>
<td>
Optional variable to enforce high number clipping
</td>
</tr>

</table>

### Parameter Summary


### Optional Module Links


### Feedbacks to the Host Model


## Setup & Configuration
<!--Previously from 'Setup Example'-->
An example `nml` block for the oxygen module is shown below:
```{}
&aed2_oxygen
   oxy_initial = 225.0
   Fsed_oxy = -40.0
   Ksed_oxy = 100.0
   theta_sed_oxy = 1.08
!  Fsed_oxy_variable = 'SDF_Fsed_oxy'
   oxy_min = 0
   oxy_max = 500
 /
```


## Case Studies & Examples

### Case Study
<!-- Previously from 'Examples' on website version -->

<center>

![Example 1: Cross-section plots comparing modelled and field salinity (psu, left) and oxygen (mg/L, right) for Sep-Dec 2008 at Swan River. The field plots are based on a contouring around 20 profile data locations.](images/oxygen_example4.png){width=75%}

</center>

<center>

![Example 2: The total area of anoxia (<2 mg O2 / L) and hypoxia (<4 mg O2 / L) within the estuary for 2008 and 2010, comparing the model (black line) and spatially interpolated weekly profile data (shaded region).](images/oxygen_example2.png){width=75%} 

</center>

### Publications




















## References

<!--chapter:end:10-dissolved_oxygen.Rmd-->

# Carbon

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:11-carbon.Rmd-->

# Nitrogen 

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:12-nitrogen.Rmd-->

# Phosphorous

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:13-phosphorous.Rmd-->

# Silica

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:14-silica.Rmd-->

# Organic Matter

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:15-organic_matter.Rmd-->

# Phytoplankton

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:16-phytoplankton.Rmd-->

# Zooplankton

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:17-zooplankton.Rmd-->

# Totals

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:18-totals.Rmd-->

# (PART)  AED+ Water Modules{-} 

# Aqueous Geochemistry

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:19-aqueous_geochemistry.Rmd-->

# Pathogens & Microbial Indicator Organisms

## Contributors
## Overview

Understanding the fate and transport of pathogenic and indicator microbes within drinking water reservoirs is critical for managers to effectively reduce risk. Over the past decade several advances have been made for the simulating organism dynamics using coupled hydrodynamic-organism fate models. These have generally been used for simulating coliform bacteria [@hipsey2008], with applications also reported for Cryptosporidium [@hipsey2004] and viruses [@sokolova2012] . In general, these models simulate organism concentrations within water bodies by accounting for external loading, advection and mixing process that occur within the lake interior, organism inactivation and sedimentation. The purpose of this document is to firstly synthesize relevant information from empirical and prior modelling studies to justify the necessary model required for reservoir systems, and secondly to summarise the implementation of the pathogen module within the AED2 model framework. 

## Model Description
###	Process Descriptions

#### General Approach {-}

The general balance equation for organism transport and fate is summarized in @hipsey2008 as: 

$$
\begin{equation}
\frac{dC}{dt} = -\frac{\partial }{\partial x_{j}}(CU_{j})+\frac{\partial }{\partial x_{j}}(\kappa_{j}\frac{\partial C}{\partial x_{j}})
+C_{in}-C_{out}+C_{r}(\tau,SS_{SED},C_{SED})\\
+[k_{g}(T,S,DOC_{L})-k_{d}(T,S,pH)-k_{l}
(I_{0},S,DO,pH)-k_{s}(T,S,SS)-k_{p}(T)]C
\end{equation}
$$

where $C$ is the organic concentration (orgs m^-3^), $t$ is time, $x_j$ is the distance in the $j$-th dimension (m), $U_j$ is the velocity in the $j$-th dimension (ms^-1^), is the eddy-diffusivity and $C_{in}$ and $C_{out}$ are the inflow and outflow fluxes respectively (orgs m^-3^s^-1^). This relates organism concentration through time to hydrodynamic characteristics within the lake (as captured by $U$, $\kappa$ and $\tau$), and the environmental conditions experienced that influence organism fate (including temperature, salinity, light intensity, dissolved organic carbon, oxygen and pH). This comprehensive description is usually simplified for specific applications, based on justification of the dominant processes present in any particular lake and available data for model setup and validation. 

Within the TUFLOWFV-AED2 model framework, the 1^st^ three terms on the RHS are solved via the finite volume scalar transport routines with TUFLOW-FV and the fourth and fifth terms are simulated by the aed2_pathogens module of the AED2 aquatic ecological modelling library. For this application the growth and predation terms suggested by @hipsey2008 are not considered directly since the likelihood of growth is small [@sidhu2012] and predation/grazing is factored into the die-off rate (described below). The remaining terms for simulation of organism resuspension and inactivation are described in detail next.

#### Natural Mortality {-}

Natural mortality, or the ‘dark-death rate’, $k_d$, is an important process determining the net rate of die off of protozoan, viral and bacterial organisms and has been reported to vary for specific organisms due to changes in temperature, salinity and pH. The reported die off rates in the literature however are widely variable, with a synthesis of numerous studies from a range of water bodies presented in @hipsey2008. For freshwater reservoirs, changes in salinity and pH are unlikely to be a significant driver of organism viability relative to the range presented @hipsey2008 and therefore a simple constant die-off rate that depends on temperature is appropriate: 

$$
k_{d}(T) = k_{d_{20}}\vartheta _{M}^{T-20}
$$

where $k_{d_{20}}$ is the rate of mortality in the dark at 20C and in freshwater. Since the AED2 implementation of the model to be applied with NPD does not include protozoan grazing as a separate term (as in Eq 1), the grazing effect needs to be embodied within the $k_{d_{20}}$ term. This effectively assumes a constant grazing pressure over time, and if chosen to be a low value this will essentially ensure conservative estimate of the die-off due to grazing. Empirical data from Wivenhoe dam shows the presence of native micro-organisms can increase the background die-off rate by 1.1-3.0x (eg Table 5 in @sidhu2012). 

#### Sunlight Inactivation {-}
Depending on the clarity of the water, the light climate of the lake can be a dominant factor influencing organism viability and this has been observed empirically in Wivenhoe Dam by @sidhu2012. Different organism types experience different sensitivity to different light bandwidths, with most organisms sensitive to UV-B and UV-A and some sensitive to light in the visible spectrum [@sinton2007]. @hipsey2008 formulated a multiple band-width model for organisms that included direct and indirect mechanisms for sunlight mediated inactivation by accounting for the effect of salinity, oxygen and pH on free radical formation. Here we use a simplified form that accounts only for direct sunlight denaturation as the indirect mechanism is more specific to MS2 phage relative to rotavirus for example [@verbyla2015]. The implemented expression is therefore: 

$$
k_{l} = \sum_{b=1}^{N_{b}}[\varphi k_{b} I_{b}]
$$

where $N_B$ is the number of discrete solar bandwidths to be modeled, $b$ is the bandwidth class {1, 2, … , $N_B$}, $k_b$ is the freshwater inactivation rate coefficient for exposure to the $b^{th}$ class (m^2^ MJ^-1^), $I_b$ is the intensity of the $b^{th}$ bandwidth class (Wm^-2^), $\varphi$ is a constant to convert units from seconds to days and J to MJ (= 8.64*10^-2^).
 
In AED2, the light intensity is computed for 3 distinct bandwidths, including UV-B, UV-A and PAR, and the attenuation of each through the reservoir water column is based on bandwidth specific light extinction coefficients, that account for the effect of turbidity and chromophoric dissolved organic matter (CDOM) on attenutation. 

#### Sedimentation {-}

Sedimentation of organisms occurs at a rate depending on the degree to which the population is attached to suspended particles. Within AED2, this is captured by simulating free and attached organisms and multiple groups of particles may be accounted for. If we assume a single dominant particle size and ignore the effect of salinity on the settling velocity, then the expression in @hipsey2008 for the effective sedimentation velocity reduces to:  
$$
k_{s}=(1-f_{a})\frac{V_{c}}{\Delta z}+f_{a}\frac{V_{s}}{\Delta z}
$$
where $f_a$ is the attached fraction, and $V$ is the vertical velocity of organisms or sediment particles.  

#### Resupension {-}

Resuspension of organisms accumulated within the sediment has been show to be a relatively important terms in environments where high currents or waves exist. In reservoirs this can occur in the lake margins or deeper in the lake where internal waves or river underflows increase the shear stress at the sediment. The amount of organisms that resuspend depends not only on the shear stress but also n the concentration of organisms in the surficial layers of the sediment. This may be modelled by accounting for the deposited organisms, decay within the sediment and resuspension rate, however, this is notoriously difficult given potentially complex dynamics of organisms in the sediment. Instead we assume that a standard background concentration exists within different sediment regions (based on depth and local geomorphology) and simulate resuspension rate as: 

$$
C_{r}(\tau)=\alpha_{c}\frac{(\tau - \tau_{c_{s}})}{\tau _{ref}}\frac{1}{\Delta z_{bot}}
$$

where, $\alpha_C$ is the rate of organism suspension (orgs m^-2^s^-1^), which occurs when the critical shear stress is exceeded in the relative computational cell. 


###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study


<!--html_preserve--><div id="htmlwidget-6799d2578071f0840364" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-6799d2578071f0840364">{"x":{"data":[{"x":[0,0.4,0.8,1.2,1.6,2,2.4,2.8,3.2,3.6,4,4.4,4.8,5.2,5.6,6,6.4,6.8,7.2,7.6,8,8.4,8.8,9.2,9.6,10,10.4,10.8,11.2,11.6,12,12.4,12.8,13.2,13.6,14,14.4,14.8,15.2,15.6,16,16.4,16.8,17.2,17.6,18,18.4,18.8,19.2,19.6,20,20.4,20.8,21.2,21.6,22,22.4,22.8,23.2,23.6,24,24.4,24.8,25.2,25.6,26,26.4,26.8,27.2,27.6,28,28.4,28.8,29.2,29.6,30,30.4,30.8,31.2,31.6,32,32.4,32.8,33.2,33.6,34,34.4,34.8,35.2,35.6,36,36.4,36.8,37.2,37.6,38,38.4,38.8,39.2,39.6,40],"y":[0.0446479950560106,0.0465008626597645,0.0484306232651579,0.0504404678900968,0.0525337199780014,0.0547138408933932,0.0569844356455458,0.0593492588496645,0.0618122209354512,0.0643773946133218,0.0670490216089678,0.0698315196773984,0.0727294899080625,0.0757477243331277,0.0788912138515006,0.0821651564816879,0.0855749659571482,0.0891262806783452,0.092824973036307,0.0966771591231076,0.100689208845328,0.104867756457221,0.109219711530997,0.113752270382369,0.118472927970253,0.123389490290298,0.128510087282745,0.133843186275949,0.139397605987804,0.145182531108219,0.151207527486756,0.157482557950553,0.164017998778676,0.170824656860149,0.177913787564035,0.185297113351117,0.192986843157947,0.20099569258533,0.209336904924612,0.21802427305656,0.227072162259013,0.236495533961063,0.246309970482999,0.256531700802961,0.267177627392888,0.278265354168146,0.289813215597051,0.301840307018421,0.314366516217288,0.327412556310987,0.341,0.355151315240191,0.369889902395417,0.38524013293196,0.401227389718743,0.417878109,0.435219824109776,0.453281211000562,0.472092135661337,0.491683703503444,0.512088310795941,0.533339698235501,0.555473006739427,0.57852483555405,0.602533302774591,0.627538108376575,0.653580599862997,0.680703840635824,0.708952681204874,0.73837383335182,0.769015947371966,0.80092969252151,0.83416784080333,0.868785354229832,0.904839475707155,0.942389823691028,0.981498490770792,1.0222301463446,1.06465214355559,1.10883463066586,1.15485066705235,1.20277634401658,1.25269091060784,1.30467690466806,1.35882028931484,1.41521059508863,1.47394106799877,1.53510882371347,1.59881500814857,1.66516496472059,1.73426840854077,1.80623960783802,1.88119757291085,1.95926625292065,2.04057474085188,2.12525748697787,2.2134545211855,2.30531168452603,2.40098087037536,2.50062027560219,2.60439466215955],"text":["y: 0.04464800<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  0.0","y: 0.04650086<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  0.4","y: 0.04843062<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  0.8","y: 0.05044047<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  1.2","y: 0.05253372<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  1.6","y: 0.05471384<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  2.0","y: 0.05698444<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  2.4","y: 0.05934926<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  2.8","y: 0.06181222<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  3.2","y: 0.06437739<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  3.6","y: 0.06704902<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  4.0","y: 0.06983152<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  4.4","y: 0.07272949<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  4.8","y: 0.07574772<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  5.2","y: 0.07889121<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  5.6","y: 0.08216516<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  6.0","y: 0.08557497<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  6.4","y: 0.08912628<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  6.8","y: 0.09282497<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  7.2","y: 0.09667716<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  7.6","y: 0.10068921<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  8.0","y: 0.10486776<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  8.4","y: 0.10921971<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  8.8","y: 0.11375227<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  9.2","y: 0.11847293<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x:  9.6","y: 0.12338949<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 10.0","y: 0.12851009<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 10.4","y: 0.13384319<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 10.8","y: 0.13939761<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 11.2","y: 0.14518253<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 11.6","y: 0.15120753<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 12.0","y: 0.15748256<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 12.4","y: 0.16401800<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 12.8","y: 0.17082466<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 13.2","y: 0.17791379<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 13.6","y: 0.18529711<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 14.0","y: 0.19298684<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 14.4","y: 0.20099569<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 14.8","y: 0.20933690<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 15.2","y: 0.21802427<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 15.6","y: 0.22707216<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 16.0","y: 0.23649553<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 16.4","y: 0.24630997<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 16.8","y: 0.25653170<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 17.2","y: 0.26717763<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 17.6","y: 0.27826535<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 18.0","y: 0.28981322<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 18.4","y: 0.30184031<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 18.8","y: 0.31436652<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 19.2","y: 0.32741256<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 19.6","y: 0.34100000<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 20.0","y: 0.35515132<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 20.4","y: 0.36988990<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 20.8","y: 0.38524013<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 21.2","y: 0.40122739<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 21.6","y: 0.41787811<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 22.0","y: 0.43521982<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 22.4","y: 0.45328121<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 22.8","y: 0.47209214<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 23.2","y: 0.49168370<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 23.6","y: 0.51208831<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 24.0","y: 0.53333970<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 24.4","y: 0.55547301<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 24.8","y: 0.57852484<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 25.2","y: 0.60253330<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 25.6","y: 0.62753811<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 26.0","y: 0.65358060<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 26.4","y: 0.68070384<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 26.8","y: 0.70895268<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 27.2","y: 0.73837383<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 27.6","y: 0.76901595<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 28.0","y: 0.80092969<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 28.4","y: 0.83416784<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 28.8","y: 0.86878535<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 29.2","y: 0.90483948<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 29.6","y: 0.94238982<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 30.0","y: 0.98149849<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 30.4","y: 1.02223015<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 30.8","y: 1.06465214<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 31.2","y: 1.10883463<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 31.6","y: 1.15485067<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 32.0","y: 1.20277634<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 32.4","y: 1.25269091<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 32.8","y: 1.30467690<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 33.2","y: 1.35882029<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 33.6","y: 1.41521060<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 34.0","y: 1.47394107<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 34.4","y: 1.53510882<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 34.8","y: 1.59881501<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 35.2","y: 1.66516496<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 35.6","y: 1.73426841<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 36.0","y: 1.80623961<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 36.4","y: 1.88119757<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 36.8","y: 1.95926625<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 37.2","y: 2.04057474<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 37.6","y: 2.12525749<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 38.0","y: 2.21345452<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 38.4","y: 2.30531168<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 38.8","y: 2.40098087<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 39.2","y: 2.50062028<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 39.6","y: 2.60439466<br />colour: Total Coliforms<br />(0.341, 1.107)<br />x: 40.0"],"type":"scatter","mode":"lines","line":{"width":1.88976377952756,"color":"rgba(245,100,227,1)","dash":"solid"},"hoveron":"points","name":"Total Coliforms<br />(0.341, 1.107)","legendgroup":"Total Coliforms<br />(0.341, 1.107)","showlegend":true,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null},{"x":[0,0.4,0.8,1.2,1.6,2,2.4,2.8,3.2,3.6,4,4.4,4.8,5.2,5.6,6,6.4,6.8,7.2,7.6,8,8.4,8.8,9.2,9.6,10,10.4,10.8,11.2,11.6,12,12.4,12.8,13.2,13.6,14,14.4,14.8,15.2,15.6,16,16.4,16.8,17.2,17.6,18,18.4,18.8,19.2,19.6,20,20.4,20.8,21.2,21.6,22,22.4,22.8,23.2,23.6,24,24.4,24.8,25.2,25.6,26,26.4,26.8,27.2,27.6,28,28.4,28.8,29.2,29.6,30,30.4,30.8,31.2,31.6,32,32.4,32.8,33.2,33.6,34,34.4,34.8,35.2,35.6,36,36.4,36.8,37.2,37.6,38,38.4,38.8,39.2,39.6,40],"y":[0.238433827941027,0.24368760435226,0.249057145237089,0.254545001410834,0.260153779894817,0.265886145154845,0.271744820366962,0.277732588711107,0.283852294693272,0.290106845496787,0.296499212363393,0.303032432004732,0.309709608044949,0.316533912495076,0.323508587259905,0.330636945678065,0.337922374096029,0.345368333476812,0.352978361044109,0.360756071962662,0.368705161055654,0.376829404559949,0.385132661919999,0.393618877621284,0.402292083064155,0.411156398478958,0.420216034883364,0.42947529608282,0.438938580715088,0.448610384339829,0.458495301574232,0.468598028275695,0.478923363772611,0.4894762131443,0.50026158955118,0.511284616616283,0.522550530859245,0.534064684183935,0.545832546420883,0.557859707925745,0.570151882235015,0.582714908780255,0.595554755662136,0.608677522485597,0.622089443257483,0.635796889348026,0.649806372517579,0.664124548010052,0.678758217714499,0.693714333396377,0.709,0.724622479023763,0.740589191969737,0.756907723869276,0.773585826886303,0.790631424,0.808052612768643,0.825857669176365,0.844055051564689,0.862653404650684,0.881661563633664,0.901088558392374,0.920943617774655,0.941236173981641,0.961975867048545,0.98317254942419,1.00483629065144,1.02697738215076,1.04960634210919,1.07273392047705,1.09637110407469,1.12052912181188,1.14521945002207,1.17045381791428,1.19624421314509,1.22260288751344,1.24954236278082,1.27707543661981,1.30521518869365,1.33397498686977,1.36336849357018,1.39340967226195,1.42411279409047,1.45549244465909,1.487563530958,1.52034128844588,1.5538412882875,1.58807944475087,1.62307202276735,1.65883564565838,1.69538730303239,1.73274435885577,1.7709245597017,1.8099460431807,1.84982734655691,1.89058741555432,1.93224561335699,1.97482172980752,2.01833599080835,2.06280906793008,2.10826208823159],"text":["y: 0.2384338<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  0.0","y: 0.2436876<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  0.4","y: 0.2490571<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  0.8","y: 0.2545450<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  1.2","y: 0.2601538<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  1.6","y: 0.2658861<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  2.0","y: 0.2717448<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  2.4","y: 0.2777326<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  2.8","y: 0.2838523<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  3.2","y: 0.2901068<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  3.6","y: 0.2964992<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  4.0","y: 0.3030324<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  4.4","y: 0.3097096<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  4.8","y: 0.3165339<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  5.2","y: 0.3235086<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  5.6","y: 0.3306369<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  6.0","y: 0.3379224<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  6.4","y: 0.3453683<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  6.8","y: 0.3529784<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  7.2","y: 0.3607561<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  7.6","y: 0.3687052<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  8.0","y: 0.3768294<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  8.4","y: 0.3851327<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  8.8","y: 0.3936189<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  9.2","y: 0.4022921<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x:  9.6","y: 0.4111564<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 10.0","y: 0.4202160<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 10.4","y: 0.4294753<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 10.8","y: 0.4389386<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 11.2","y: 0.4486104<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 11.6","y: 0.4584953<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 12.0","y: 0.4685980<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 12.4","y: 0.4789234<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 12.8","y: 0.4894762<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 13.2","y: 0.5002616<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 13.6","y: 0.5112846<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 14.0","y: 0.5225505<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 14.4","y: 0.5340647<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 14.8","y: 0.5458325<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 15.2","y: 0.5578597<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 15.6","y: 0.5701519<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 16.0","y: 0.5827149<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 16.4","y: 0.5955548<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 16.8","y: 0.6086775<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 17.2","y: 0.6220894<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 17.6","y: 0.6357969<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 18.0","y: 0.6498064<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 18.4","y: 0.6641245<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 18.8","y: 0.6787582<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 19.2","y: 0.6937143<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 19.6","y: 0.7090000<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 20.0","y: 0.7246225<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 20.4","y: 0.7405892<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 20.8","y: 0.7569077<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 21.2","y: 0.7735858<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 21.6","y: 0.7906314<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 22.0","y: 0.8080526<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 22.4","y: 0.8258577<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 22.8","y: 0.8440551<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 23.2","y: 0.8626534<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 23.6","y: 0.8816616<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 24.0","y: 0.9010886<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 24.4","y: 0.9209436<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 24.8","y: 0.9412362<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 25.2","y: 0.9619759<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 25.6","y: 0.9831725<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 26.0","y: 1.0048363<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 26.4","y: 1.0269774<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 26.8","y: 1.0496063<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 27.2","y: 1.0727339<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 27.6","y: 1.0963711<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 28.0","y: 1.1205291<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 28.4","y: 1.1452195<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 28.8","y: 1.1704538<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 29.2","y: 1.1962442<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 29.6","y: 1.2226029<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 30.0","y: 1.2495424<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 30.4","y: 1.2770754<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 30.8","y: 1.3052152<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 31.2","y: 1.3339750<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 31.6","y: 1.3633685<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 32.0","y: 1.3934097<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 32.4","y: 1.4241128<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 32.8","y: 1.4554924<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 33.2","y: 1.4875635<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 33.6","y: 1.5203413<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 34.0","y: 1.5538413<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 34.4","y: 1.5880794<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 34.8","y: 1.6230720<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 35.2","y: 1.6588356<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 35.6","y: 1.6953873<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 36.0","y: 1.7327444<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 36.4","y: 1.7709246<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 36.8","y: 1.8099460<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 37.2","y: 1.8498273<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 37.6","y: 1.8905874<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 38.0","y: 1.9322456<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 38.4","y: 1.9748217<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 38.8","y: 2.0183360<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 39.2","y: 2.0628091<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 39.6","y: 2.1082621<br />colour: Faecal Coliforms<br />(0.709, 1.056)<br />x: 40.0"],"type":"scatter","mode":"lines","line":{"width":1.88976377952756,"color":"rgba(0,191,196,1)","dash":"solid"},"hoveron":"points","name":"Faecal Coliforms<br />(0.709, 1.056)","legendgroup":"Faecal Coliforms<br />(0.709, 1.056)","showlegend":true,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null},{"x":[0,0.4,0.8,1.2,1.6,2,2.4,2.8,3.2,3.6,4,4.4,4.8,5.2,5.6,6,6.4,6.8,7.2,7.6,8,8.4,8.8,9.2,9.6,10,10.4,10.8,11.2,11.6,12,12.4,12.8,13.2,13.6,14,14.4,14.8,15.2,15.6,16,16.4,16.8,17.2,17.6,18,18.4,18.8,19.2,19.6,20,20.4,20.8,21.2,21.6,22,22.4,22.8,23.2,23.6,24,24.4,24.8,25.2,25.6,26,26.4,26.8,27.2,27.6,28,28.4,28.8,29.2,29.6,30,30.4,30.8,31.2,31.6,32,32.4,32.8,33.2,33.6,34,34.4,34.8,35.2,35.6,36,36.4,36.8,37.2,37.6,38,38.4,38.8,39.2,39.6,40],"y":[0.0587172705578653,0.0612422986482183,0.0638759109216659,0.0666227768410404,0.0694877666708242,0.0724759601122549,0.0755926553097675,0.0788433782447416,0.0822338925332099,0.0857702096448984,0.0894585995617186,0.0933056018946075,0.0973180374784277,0.101503020465484,0.105867970939101,0.11042062806962,0.115169063836154,0.12012169733841,0.125287309723977,0.130675059757522,0.136294500059521,0.142155594043305,0.148268733580444,0.154644757425809,0.161294970434964,0.168231163607969,0.175465634995127,0.183011211501747,0.190881271630582,0.199089769202255,0.207651258095751,0.21658091805282,0.225894581592048,0.235608762080331,0.245740683011497,0.256308308544006,0.267330375351874,0.278826425845278,0.290816842819757,0.303322885595433,0.316366727710346,0.329971496234701,0.34416131277577,0.358961336246125,0.374397807471041,0.390498095714162,0.407290747203912,0.424805535746701,0.443073515516653,0.462127076115463,0.482,0.50272752237948,0.524346393688404,0.546894944746031,0.570413154717914,0.594942722,0.620527138150962,0.647211765003864,0.675043915093865,0.704072935544571,0.734350295561762,0.765929677689634,0.798867072991335,0.833220880322575,0.86905200987431,0.90642399116809,0.945403085695547,0.986058404401737,1.02846203022064,1.07268914588007,1.11881816720259,1.16693088213881,1.21711259577956,1.26945228160397,1.32404273923183,1.38098075895966,1.44036729337246,1.50230763633522,1.5669116096817,1.63429375793137,1.70457355137985,1.77787559792279,1.85432986398892,1.93407190497392,2.01724310558361,2.10399093051273,2.19446918590366,2.28883829204867,2.38726556781931,2.48992552732707,2.5970001893414,2.70867940001379,2.82516116947981,2.9466520229363,3.07336736681587,3.20553187070807,3.34337986570442,3.48715575987349,3.63711447160276,3.79352188157554,3.95665530418426],"text":["y: 0.05871727<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  0.0","y: 0.06124230<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  0.4","y: 0.06387591<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  0.8","y: 0.06662278<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  1.2","y: 0.06948777<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  1.6","y: 0.07247596<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  2.0","y: 0.07559266<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  2.4","y: 0.07884338<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  2.8","y: 0.08223389<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  3.2","y: 0.08577021<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  3.6","y: 0.08945860<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  4.0","y: 0.09330560<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  4.4","y: 0.09731804<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  4.8","y: 0.10150302<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  5.2","y: 0.10586797<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  5.6","y: 0.11042063<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  6.0","y: 0.11516906<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  6.4","y: 0.12012170<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  6.8","y: 0.12528731<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  7.2","y: 0.13067506<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  7.6","y: 0.13629450<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  8.0","y: 0.14215559<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  8.4","y: 0.14826873<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  8.8","y: 0.15464476<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  9.2","y: 0.16129497<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x:  9.6","y: 0.16823116<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 10.0","y: 0.17546563<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 10.4","y: 0.18301121<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 10.8","y: 0.19088127<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 11.2","y: 0.19908977<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 11.6","y: 0.20765126<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 12.0","y: 0.21658092<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 12.4","y: 0.22589458<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 12.8","y: 0.23560876<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 13.2","y: 0.24574068<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 13.6","y: 0.25630831<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 14.0","y: 0.26733038<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 14.4","y: 0.27882643<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 14.8","y: 0.29081684<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 15.2","y: 0.30332289<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 15.6","y: 0.31636673<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 16.0","y: 0.32997150<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 16.4","y: 0.34416131<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 16.8","y: 0.35896134<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 17.2","y: 0.37439781<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 17.6","y: 0.39049810<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 18.0","y: 0.40729075<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 18.4","y: 0.42480554<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 18.8","y: 0.44307352<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 19.2","y: 0.46212708<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 19.6","y: 0.48200000<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 20.0","y: 0.50272752<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 20.4","y: 0.52434639<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 20.8","y: 0.54689494<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 21.2","y: 0.57041315<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 21.6","y: 0.59494272<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 22.0","y: 0.62052714<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 22.4","y: 0.64721177<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 22.8","y: 0.67504392<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 23.2","y: 0.70407294<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 23.6","y: 0.73435030<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 24.0","y: 0.76592968<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 24.4","y: 0.79886707<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 24.8","y: 0.83322088<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 25.2","y: 0.86905201<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 25.6","y: 0.90642399<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 26.0","y: 0.94540309<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 26.4","y: 0.98605840<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 26.8","y: 1.02846203<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 27.2","y: 1.07268915<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 27.6","y: 1.11881817<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 28.0","y: 1.16693088<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 28.4","y: 1.21711260<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 28.8","y: 1.26945228<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 29.2","y: 1.32404274<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 29.6","y: 1.38098076<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 30.0","y: 1.44036729<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 30.4","y: 1.50230764<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 30.8","y: 1.56691161<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 31.2","y: 1.63429376<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 31.6","y: 1.70457355<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 32.0","y: 1.77787560<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 32.4","y: 1.85432986<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 32.8","y: 1.93407190<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 33.2","y: 2.01724311<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 33.6","y: 2.10399093<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 34.0","y: 2.19446919<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 34.4","y: 2.28883829<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 34.8","y: 2.38726557<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 35.2","y: 2.48992553<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 35.6","y: 2.59700019<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 36.0","y: 2.70867940<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 36.4","y: 2.82516117<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 36.8","y: 2.94665202<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 37.2","y: 3.07336737<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 37.6","y: 3.20553187<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 38.0","y: 3.34337987<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 38.4","y: 3.48715576<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 38.8","y: 3.63711447<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 39.2","y: 3.79352188<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 39.6","y: 3.95665530<br />colour: <i>E.coli<\/i><br />(0.482, 1.111)<br />x: 40.0"],"type":"scatter","mode":"lines","line":{"width":1.88976377952756,"color":"rgba(248,118,109,1)","dash":"solid"},"hoveron":"points","name":"<i>E.coli<\/i><br />(0.482, 1.111)","legendgroup":"<i>E.coli<\/i><br />(0.482, 1.111)","showlegend":true,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null},{"x":[0,0.4,0.8,1.2,1.6,2,2.4,2.8,3.2,3.6,4,4.4,4.8,5.2,5.6,6,6.4,6.8,7.2,7.6,8,8.4,8.8,9.2,9.6,10,10.4,10.8,11.2,11.6,12,12.4,12.8,13.2,13.6,14,14.4,14.8,15.2,15.6,16,16.4,16.8,17.2,17.6,18,18.4,18.8,19.2,19.6,20,20.4,20.8,21.2,21.6,22,22.4,22.8,23.2,23.6,24,24.4,24.8,25.2,25.6,26,26.4,26.8,27.2,27.6,28,28.4,28.8,29.2,29.6,30,30.4,30.8,31.2,31.6,32,32.4,32.8,33.2,33.6,34,34.4,34.8,35.2,35.6,36,36.4,36.8,37.2,37.6,38,38.4,38.8,39.2,39.6,40],"y":[0.191887144247254,0.195220795888138,0.19861236299442,0.202062851730357,0.205573285740281,0.209144706452275,0.212778173387134,0.216474764472686,0.220235576363578,0.224061724766619,0.227954344771767,0.231914591188879,0.235943638890301,0.240042683159413,0.244212940045229,0.24845564672316,0.252772061862042,0.25716346599754,0.261631161912038,0.266176475021137,0.270800753766855,0.275505370017667,0.280291719475494,0.285161222089759,0.290115322478638,0.29515549035763,0.300283220975576,0.305500035558242,0.310807481759624,0.316207134121077,0.321700594538434,0.327289492737235,0.332975486756209,0.338760263439157,0.34464553893539,0.350633059208843,0.356724600556051,0.362921970133115,0.369227006491821,0.375641580125083,0.38216759402185,0.388806984231661,0.395561720439007,0.40243380654767,0.409425281275213,0.416538218757799,0.423774729165519,0.431136959328409,0.438627093373341,0.44624735337198,0.454,0.461887333207749,0.469911692902569,0.478075459642966,0.486381055344843,0.494830944,0.503427632407122,0.512173670915455,0.521071654181416,0.530124221938336,0.539334059779584,0.548703899955288,0.558236522182907,0.567934754471876,0.577801473962583,0.587839607779921,0.598052133901667,0.608442082041949,0.619012534550058,0.629766627324881,0.640707550745216,0.651838550616248,0.663162929132474,0.674684045857352,0.686405318719972,0.698330225029038,0.710462302504471,0.722805150326932,0.735362430205579,0.748137867464371,0.761135252147249,0.774358440142513,0.787811354326735,0.801497985728548,0.815422394712647,0.829588712184364,0.84400114081517,0.858663956289465,0.873581508573031,0.888758223203524,0.904198602603377,0.919907227415523,0.935888757862314,0.952147935128056,0.968689582765556,0.985518608127115,1.00264000382037,1.02005884918942,1.03778031182173,1.05580964908116,1.07415220966764],"text":["y: 0.1918871<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  0.0","y: 0.1952208<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  0.4","y: 0.1986124<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  0.8","y: 0.2020629<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  1.2","y: 0.2055733<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  1.6","y: 0.2091447<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  2.0","y: 0.2127782<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  2.4","y: 0.2164748<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  2.8","y: 0.2202356<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  3.2","y: 0.2240617<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  3.6","y: 0.2279543<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  4.0","y: 0.2319146<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  4.4","y: 0.2359436<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  4.8","y: 0.2400427<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  5.2","y: 0.2442129<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  5.6","y: 0.2484556<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  6.0","y: 0.2527721<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  6.4","y: 0.2571635<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  6.8","y: 0.2616312<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  7.2","y: 0.2661765<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  7.6","y: 0.2708008<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  8.0","y: 0.2755054<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  8.4","y: 0.2802917<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  8.8","y: 0.2851612<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  9.2","y: 0.2901153<br />colour: Enterococci<br />(0.454, 1.044)<br />x:  9.6","y: 0.2951555<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 10.0","y: 0.3002832<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 10.4","y: 0.3055000<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 10.8","y: 0.3108075<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 11.2","y: 0.3162071<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 11.6","y: 0.3217006<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 12.0","y: 0.3272895<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 12.4","y: 0.3329755<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 12.8","y: 0.3387603<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 13.2","y: 0.3446455<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 13.6","y: 0.3506331<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 14.0","y: 0.3567246<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 14.4","y: 0.3629220<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 14.8","y: 0.3692270<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 15.2","y: 0.3756416<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 15.6","y: 0.3821676<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 16.0","y: 0.3888070<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 16.4","y: 0.3955617<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 16.8","y: 0.4024338<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 17.2","y: 0.4094253<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 17.6","y: 0.4165382<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 18.0","y: 0.4237747<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 18.4","y: 0.4311370<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 18.8","y: 0.4386271<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 19.2","y: 0.4462474<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 19.6","y: 0.4540000<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 20.0","y: 0.4618873<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 20.4","y: 0.4699117<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 20.8","y: 0.4780755<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 21.2","y: 0.4863811<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 21.6","y: 0.4948309<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 22.0","y: 0.5034276<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 22.4","y: 0.5121737<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 22.8","y: 0.5210717<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 23.2","y: 0.5301242<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 23.6","y: 0.5393341<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 24.0","y: 0.5487039<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 24.4","y: 0.5582365<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 24.8","y: 0.5679348<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 25.2","y: 0.5778015<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 25.6","y: 0.5878396<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 26.0","y: 0.5980521<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 26.4","y: 0.6084421<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 26.8","y: 0.6190125<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 27.2","y: 0.6297666<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 27.6","y: 0.6407076<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 28.0","y: 0.6518386<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 28.4","y: 0.6631629<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 28.8","y: 0.6746840<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 29.2","y: 0.6864053<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 29.6","y: 0.6983302<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 30.0","y: 0.7104623<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 30.4","y: 0.7228052<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 30.8","y: 0.7353624<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 31.2","y: 0.7481379<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 31.6","y: 0.7611353<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 32.0","y: 0.7743584<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 32.4","y: 0.7878114<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 32.8","y: 0.8014980<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 33.2","y: 0.8154224<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 33.6","y: 0.8295887<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 34.0","y: 0.8440011<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 34.4","y: 0.8586640<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 34.8","y: 0.8735815<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 35.2","y: 0.8887582<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 35.6","y: 0.9041986<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 36.0","y: 0.9199072<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 36.4","y: 0.9358888<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 36.8","y: 0.9521479<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 37.2","y: 0.9686896<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 37.6","y: 0.9855186<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 38.0","y: 1.0026400<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 38.4","y: 1.0200588<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 38.8","y: 1.0377803<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 39.2","y: 1.0558096<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 39.6","y: 1.0741522<br />colour: Enterococci<br />(0.454, 1.044)<br />x: 40.0"],"type":"scatter","mode":"lines","line":{"width":1.88976377952756,"color":"rgba(183,159,0,1)","dash":"solid"},"hoveron":"points","name":"Enterococci<br />(0.454, 1.044)","legendgroup":"Enterococci<br />(0.454, 1.044)","showlegend":true,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null},{"x":[0,0.4,0.8,1.2,1.6,2,2.4,2.8,3.2,3.6,4,4.4,4.8,5.2,5.6,6,6.4,6.8,7.2,7.6,8,8.4,8.8,9.2,9.6,10,10.4,10.8,11.2,11.6,12,12.4,12.8,13.2,13.6,14,14.4,14.8,15.2,15.6,16,16.4,16.8,17.2,17.6,18,18.4,18.8,19.2,19.6,20,20.4,20.8,21.2,21.6,22,22.4,22.8,23.2,23.6,24,24.4,24.8,25.2,25.6,26,26.4,26.8,27.2,27.6,28,28.4,28.8,29.2,29.6,30,30.4,30.8,31.2,31.6,32,32.4,32.8,33.2,33.6,34,34.4,34.8,35.2,35.6,36,36.4,36.8,37.2,37.6,38,38.4,38.8,39.2,39.6,40],"y":[0.04902236009276,0.0509643927107971,0.0529833594193673,0.0550823079810216,0.0572644068961596,0.0595329501860881,0.0618913623655629,0.0643432036123174,0.0668921751413846,0.0695421247923238,0.0722970528377862,0.0751611180221891,0.0781386438396127,0.081234125060398,0.0844522345162972,0.0877978301544189,0.0912759623706185,0.0948918816334011,0.0986510464098476,0.102559131405529,0.106622036130847,0.110845893806729,0.115237080623129,0.119802225364305,0.1245482194154,0.129482227165445,0.134611696822466,0.13994437165705,0.145488301691313,0.15125185585094,0.157243734598625,0.163472983067991,0.169949004717808,0.176681575527137,0.183680858752805,0.190957420271509,0.1985222445297,0.206386751125325,0.214562812046458,0.223062769592841,0.231899455007401,0.241086207845846,0.2506368961136,0.260565937200466,0.270888319644625,0.281619625758808,0.292776055152827,0.30437444918794,0.316432316399995,0.328967858929711,0.342,0.355548412481814,0.369633548591631,0.38427667076542,0.399499883755677,0.415326168,0.431779414311564,0.448884459943871,0.466667126084209,0.48515425683243,0.504373759723872,0.524354647857621,0.545127083693677,0.566722424585168,0.58917327011433,0.612513511303709,0.636778381776887,0.662004510945936,0.688229979305927,0.715494375919923,0.74383885818127,0.773306213943378,0.803940926110789,0.835789239789035,0.868899232094658,0.903320884730767,0.939106159437695,0.976309076432646,1.01498579595676,1.05519470305268,1.09699649570058,1.14045427644577,1.18563364765611,1.23260281055308,1.28143266816599,1.33219693236477,1.38497223513285,1.43983824424817,1.4968777835469,1.55617695795145,1.61782528345151,1.68191582223428,1.74854532316796,1.81781436785049,1.88982752244407,1.96469349552464,2.0425253021846,2.12344043463646,2.20756103957511,2.29501410256617,2.38593163973911],"text":["y: 0.04902236<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  0.0","y: 0.05096439<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  0.4","y: 0.05298336<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  0.8","y: 0.05508231<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  1.2","y: 0.05726441<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  1.6","y: 0.05953295<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  2.0","y: 0.06189136<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  2.4","y: 0.06434320<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  2.8","y: 0.06689218<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  3.2","y: 0.06954212<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  3.6","y: 0.07229705<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  4.0","y: 0.07516112<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  4.4","y: 0.07813864<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  4.8","y: 0.08123413<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  5.2","y: 0.08445223<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  5.6","y: 0.08779783<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  6.0","y: 0.09127596<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  6.4","y: 0.09489188<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  6.8","y: 0.09865105<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  7.2","y: 0.10255913<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  7.6","y: 0.10662204<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  8.0","y: 0.11084589<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  8.4","y: 0.11523708<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  8.8","y: 0.11980223<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  9.2","y: 0.12454822<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x:  9.6","y: 0.12948223<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 10.0","y: 0.13461170<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 10.4","y: 0.13994437<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 10.8","y: 0.14548830<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 11.2","y: 0.15125186<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 11.6","y: 0.15724373<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 12.0","y: 0.16347298<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 12.4","y: 0.16994900<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 12.8","y: 0.17668158<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 13.2","y: 0.18368086<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 13.6","y: 0.19095742<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 14.0","y: 0.19852224<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 14.4","y: 0.20638675<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 14.8","y: 0.21456281<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 15.2","y: 0.22306277<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 15.6","y: 0.23189946<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 16.0","y: 0.24108621<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 16.4","y: 0.25063690<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 16.8","y: 0.26056594<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 17.2","y: 0.27088832<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 17.6","y: 0.28161963<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 18.0","y: 0.29277606<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 18.4","y: 0.30437445<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 18.8","y: 0.31643232<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 19.2","y: 0.32896786<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 19.6","y: 0.34200000<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 20.0","y: 0.35554841<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 20.4","y: 0.36963355<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 20.8","y: 0.38427667<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 21.2","y: 0.39949988<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 21.6","y: 0.41532617<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 22.0","y: 0.43177941<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 22.4","y: 0.44888446<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 22.8","y: 0.46666713<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 23.2","y: 0.48515426<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 23.6","y: 0.50437376<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 24.0","y: 0.52435465<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 24.4","y: 0.54512708<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 24.8","y: 0.56672242<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 25.2","y: 0.58917327<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 25.6","y: 0.61251351<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 26.0","y: 0.63677838<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 26.4","y: 0.66200451<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 26.8","y: 0.68822998<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 27.2","y: 0.71549438<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 27.6","y: 0.74383886<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 28.0","y: 0.77330621<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 28.4","y: 0.80394093<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 28.8","y: 0.83578924<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 29.2","y: 0.86889923<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 29.6","y: 0.90332088<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 30.0","y: 0.93910616<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 30.4","y: 0.97630908<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 30.8","y: 1.01498580<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 31.2","y: 1.05519470<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 31.6","y: 1.09699650<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 32.0","y: 1.14045428<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 32.4","y: 1.18563365<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 32.8","y: 1.23260281<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 33.2","y: 1.28143267<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 33.6","y: 1.33219693<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 34.0","y: 1.38497224<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 34.4","y: 1.43983824<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 34.8","y: 1.49687778<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 35.2","y: 1.55617696<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 35.6","y: 1.61782528<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 36.0","y: 1.68191582<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 36.4","y: 1.74854532<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 36.8","y: 1.81781437<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 37.2","y: 1.88982752<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 37.6","y: 1.96469350<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 38.0","y: 2.04252530<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 38.4","y: 2.12344043<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 38.8","y: 2.20756104<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 39.2","y: 2.29501410<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 39.6","y: 2.38593164<br />colour: F+RNA Phages<br />(0.342, 1.102)<br />x: 40.0"],"type":"scatter","mode":"lines","line":{"width":1.88976377952756,"color":"rgba(0,186,56,1)","dash":"solid"},"hoveron":"points","name":"F+RNA Phages<br />(0.342, 1.102)","legendgroup":"F+RNA Phages<br />(0.342, 1.102)","showlegend":true,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null},{"x":[0,0.4,0.8,1.2,1.6,2,2.4,2.8,3.2,3.6,4,4.4,4.8,5.2,5.6,6,6.4,6.8,7.2,7.6,8,8.4,8.8,9.2,9.6,10,10.4,10.8,11.2,11.6,12,12.4,12.8,13.2,13.6,14,14.4,14.8,15.2,15.6,16,16.4,16.8,17.2,17.6,18,18.4,18.8,19.2,19.6,20,20.4,20.8,21.2,21.6,22,22.4,22.8,23.2,23.6,24,24.4,24.8,25.2,25.6,26,26.4,26.8,27.2,27.6,28,28.4,28.8,29.2,29.6,30,30.4,30.8,31.2,31.6,32,32.4,32.8,33.2,33.6,34,34.4,34.8,35.2,35.6,36,36.4,36.8,37.2,37.6,38,38.4,38.8,39.2,39.6,40],"y":[0.134405293135316,0.134941309990766,0.135479464515518,0.136019765234735,0.136562220707576,0.137106839527336,0.13765363032158,0.13820260175228,0.138753762515953,0.139307121343799,0.139862687001836,0.140420468291044,0.140980474047501,0.141542713142524,0.142107194482809,0.142673927010573,0.143242919703694,0.143814181575856,0.144387721676689,0.144963549091913,0.145541672943485,0.146122102389738,0.146704846625531,0.14728991488239,0.147877316428661,0.148467060569649,0.149059156647772,0.149653614042704,0.150250442171526,0.150849650488877,0.151451248487099,0.152055245696392,0.152661651684962,0.153270476059174,0.153881728463703,0.15449541858169,0.15511155613489,0.15573015088383,0.156351212627963,0.156974751205824,0.157600776495182,0.158229298413201,0.158860326916595,0.159493872001785,0.160129943705061,0.160768552102735,0.161409707311306,0.162053419487618,0.162699698829021,0.163348555573533,0.164,0.164654042428263,0.165310693219319,0.165969962775485,0.166631861540561,0.1672964,0.167963588681072,0.168633438153028,0.169305959027272,0.169981161957526,0.17065905764,0.171339656813561,0.172022970259904,0.17270900880372,0.173397783312872,0.174089304698564,0.174783583915514,0.175480631962128,0.176180459880675,0.176883078757461,0.177588499723005,0.178296733952216,0.179007792664566,0.179721687124276,0.180438428640486,0.181158028567438,0.181880498304655,0.182605849297124,0.183334093035474,0.18406524105616,0.184799304941643,0.185536296320579,0.186276226867996,0.187019108305487,0.187764952401388,0.18851377097097,0.189265575876622,0.190020379028043,0.190778192382428,0.191539027944656,0.192302897767487,0.193069813951742,0.193839788646507,0.194612834049314,0.195388962406344,0.196168186012613,0.196950517212172,0.197735968398302,0.198524552013706,0.199316280550712,0.200111166551467],"text":["y: 0.1344053<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  0.0","y: 0.1349413<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  0.4","y: 0.1354795<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  0.8","y: 0.1360198<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  1.2","y: 0.1365622<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  1.6","y: 0.1371068<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  2.0","y: 0.1376536<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  2.4","y: 0.1382026<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  2.8","y: 0.1387538<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  3.2","y: 0.1393071<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  3.6","y: 0.1398627<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  4.0","y: 0.1404205<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  4.4","y: 0.1409805<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  4.8","y: 0.1415427<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  5.2","y: 0.1421072<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  5.6","y: 0.1426739<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  6.0","y: 0.1432429<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  6.4","y: 0.1438142<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  6.8","y: 0.1443877<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  7.2","y: 0.1449635<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  7.6","y: 0.1455417<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  8.0","y: 0.1461221<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  8.4","y: 0.1467048<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  8.8","y: 0.1472899<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  9.2","y: 0.1478773<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x:  9.6","y: 0.1484671<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 10.0","y: 0.1490592<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 10.4","y: 0.1496536<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 10.8","y: 0.1502504<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 11.2","y: 0.1508497<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 11.6","y: 0.1514512<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 12.0","y: 0.1520552<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 12.4","y: 0.1526617<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 12.8","y: 0.1532705<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 13.2","y: 0.1538817<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 13.6","y: 0.1544954<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 14.0","y: 0.1551116<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 14.4","y: 0.1557302<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 14.8","y: 0.1563512<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 15.2","y: 0.1569748<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 15.6","y: 0.1576008<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 16.0","y: 0.1582293<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 16.4","y: 0.1588603<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 16.8","y: 0.1594939<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 17.2","y: 0.1601299<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 17.6","y: 0.1607686<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 18.0","y: 0.1614097<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 18.4","y: 0.1620534<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 18.8","y: 0.1626997<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 19.2","y: 0.1633486<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 19.6","y: 0.1640000<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 20.0","y: 0.1646540<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 20.4","y: 0.1653107<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 20.8","y: 0.1659700<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 21.2","y: 0.1666319<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 21.6","y: 0.1672964<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 22.0","y: 0.1679636<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 22.4","y: 0.1686334<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 22.8","y: 0.1693060<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 23.2","y: 0.1699812<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 23.6","y: 0.1706591<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 24.0","y: 0.1713397<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 24.4","y: 0.1720230<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 24.8","y: 0.1727090<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 25.2","y: 0.1733978<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 25.6","y: 0.1740893<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 26.0","y: 0.1747836<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 26.4","y: 0.1754806<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 26.8","y: 0.1761805<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 27.2","y: 0.1768831<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 27.6","y: 0.1775885<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 28.0","y: 0.1782967<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 28.4","y: 0.1790078<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 28.8","y: 0.1797217<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 29.2","y: 0.1804384<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 29.6","y: 0.1811580<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 30.0","y: 0.1818805<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 30.4","y: 0.1826058<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 30.8","y: 0.1833341<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 31.2","y: 0.1840652<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 31.6","y: 0.1847993<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 32.0","y: 0.1855363<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 32.4","y: 0.1862762<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 32.8","y: 0.1870191<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 33.2","y: 0.1877650<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 33.6","y: 0.1885138<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 34.0","y: 0.1892656<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 34.4","y: 0.1900204<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 34.8","y: 0.1907782<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 35.2","y: 0.1915390<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 35.6","y: 0.1923029<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 36.0","y: 0.1930698<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 36.4","y: 0.1938398<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 36.8","y: 0.1946128<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 37.2","y: 0.1953890<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 37.6","y: 0.1961682<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 38.0","y: 0.1969505<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 38.4","y: 0.1977360<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 38.8","y: 0.1985246<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 39.2","y: 0.1993163<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 39.6","y: 0.2001112<br />colour: Somatic Coliphages<br />(0.164,1.010)<br />x: 40.0"],"type":"scatter","mode":"lines","line":{"width":1.88976377952756,"color":"rgba(97,156,255,1)","dash":"solid"},"hoveron":"points","name":"Somatic Coliphages<br />(0.164,1.010)","legendgroup":"Somatic Coliphages<br />(0.164,1.010)","showlegend":true,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null}],"layout":{"margin":{"t":26.2283105022831,"r":7.30593607305936,"b":40.1826484018265,"l":31.4155251141553},"plot_bgcolor":"rgba(255,255,255,1)","paper_bgcolor":"rgba(255,255,255,1)","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187},"xaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[-2,42],"tickmode":"array","ticktext":["0","10","20","30","40"],"tickvals":[0,10,20,30,40],"categoryorder":"array","categoryarray":["0","10","20","30","40"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(235,235,235,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"y","title":{"text":"Temperature (˚C)","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"yaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[-0.150952370400402,4.15225566964067],"tickmode":"array","ticktext":["0","1","2","3","4"],"tickvals":[0,1,2,3,4],"categoryorder":"array","categoryarray":["0","1","2","3","4"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(235,235,235,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"x","title":{"text":"k<sub>d<\/sub>(T,0,7)(day<sup>-1<\/sup>)","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"shapes":[{"type":"rect","fillcolor":"transparent","line":{"color":"rgba(51,51,51,1)","width":0.66417600664176,"linetype":"solid"},"yref":"paper","xref":"paper","x0":0,"x1":1,"y0":0,"y1":1}],"showlegend":true,"legend":{"bgcolor":"rgba(255,255,255,1)","bordercolor":"transparent","borderwidth":1.88976377952756,"font":{"color":"rgba(0,0,0,1)","family":"","size":11.689497716895},"y":1,"x":1},"annotations":[{"text":"Organism Group","x":1.02,"y":1,"showarrow":false,"ax":0,"ay":0,"font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187},"xref":"paper","yref":"paper","textangle":-0,"xanchor":"left","yanchor":"bottom","legendTitle":true}],"hovermode":"closest","barmode":"relative"},"config":{"doubleClick":"reset","showSendToCloud":false},"source":"A","attrs":{"177953531ef95":{"colour":{},"x":{},"type":"scatter"},"1779561683a7b":{"colour":{},"x":{}},"177951d79333":{"colour":{},"x":{}},"177957000fa36":{"colour":{},"x":{}},"17795502b28ac":{"colour":{},"x":{}},"17795417b5d52":{"colour":{},"x":{}}},"cur_data":"177953531ef95","visdat":{"177953531ef95":["function (y) ","x"],"1779561683a7b":["function (y) ","x"],"177951d79333":["function (y) ","x"],"177957000fa36":["function (y) ","x"],"17795502b28ac":["function (y) ","x"],"17795417b5d52":["function (y) ","x"]},"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->


###	Publications

## References





<!--chapter:end:20-pathogens_microbial_indicators.Rmd-->

# Stable Isotopes

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:21-stable_isotopes.Rmd-->

# Bioactive Particles

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:22-bioactive_particles.Rmd-->

# (PART) AED+ Benthic Modules {-} 

# Sediment Biogeochemistry

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:23-sediment_biogeochemistry.Rmd-->

# Submerged Macrophytes

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:24-submerged_macrophytes.Rmd-->

# Macroalgae

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:25-macroalgae.Rmd-->

# Bivalves

## Contributors
## Overview

Based on work in freshwater and estuarine systems a bivalve module to simulate growth, production, and (optionally) population dynamics has been incorporated into the AED2+ library.

The model is originally based on an application to Oneida Lake and Lake Erie for mussels. One to several size classes of mussels are simulated based on physiological parameters assembled by @schneider1992 and modified by @bierman2005 to estimate effect of mussels on Saginaw Bay, Michigan, USA; a formulation also used by @gudimov2015 to estimate mussel effects in Lake Simcoe, Ontario, Canada.  Additionally, some model structure was taken from the @spillman2008 model of Tapes clams in the Barbamarco Lagoon, Italy, as modified by @bocaniov2014 for mussels in Lake Erie. 

The physiology of mussels are set to be size dependent, and can vary between species (e.g., Zebra vs Quagga)(Hetherington, 2016).  Three size classes of mussels can be incorporated in the model, roughly corresponding to age-0, age-1 and age>1 mussels.  Physiological parameters are calculated for the weight assigned to each age class, using equations in Table 4.  Individual mussel mass is given in mmol C or in the case of calculations of N and P budgets, in mmol N and mmol P.  The stoichiometric ratios (C:N:P) are fixed.  Group mussel biomass is calculated at each time step by calculating ingestion and subtracting pseudofeces production, standard dynamic action, respiration, excretion, egestion and mortality (expressed in mmol C/mmol C/day, mmol N/mmol N/day; mmol P/mmol P/day).  Several of these processes are also functions of temperature, algal+POC concentrations, salinity, suspended solids and mussel density.  The effect of salinity, suspended solids and mussel density is incorporated as a multiplier of filtration rate with the multipliers having values between -0 – (no filtering) and 1 (no effect). Mussel nitrogen and phosphorus concentrations are fixed ratios of mussel carbon concentrations. Since the various input and output fluxes have variable C:N:P ratios, the excretion of nutrients is dynamically adjusted each time-step to maintain this ratio at each time step.  Reproduction and larval dynamics are not simulated. There is no transfer of biomass between age groups.

## Model Description
###	Process Descriptions

#### Ingestion {-}
Ingestion is modelled as a function of filtration rate, food availability, pseudofeces production, density, suspended solids, and salinity (Equation 2) [@schneider1992; @bierman2005; @spillman2008; @gudimov2015]. Filtration rate is based on maximum ingestion, temperature, food availability, and pseudofeces production according to the following:
<center>
<br>
\begin{equation}
FR = \frac{\frac{I_{max}*f(T)_{I}}{K_{A}}}{PF_{min}} \text{ for } [A] < KA
(\#eq:bivalve1)
\end{equation}
</center>
<br>
<center>
\begin{equation}
FR = \frac{\frac{I_{max}*f(T)_{I}}{[A]}}{PF_{min}} \text{ for } [A] > KA
(\#eq:bivalve2)
\end{equation}
</center>
<br>

where $FR$ is filtration rate (mmol/mmol/d), $Imax$ is maximum ingestion rate (mmol/mmol/d), $f(T)_{I}$ is filtration temperature function, $K_{A}$ is optimum algal concentration (mmol/m3), $[A]$ is algal concentration + particulate organic carbon (POC) concentration (mmol/m3), and $PFmin$ is minimum pseudofeces production (-).
The maximum ingestion rate is based on weight from length according to the following:

<center>
<br>
\begin{equation}
I_{max} = (a_{I} * W^{bI})
(\#eq:bivalve3)
\end{equation}
</center>
<br>
<center>
\begin{equation}
W = \frac{0.071}{1000} * L^{2.8}
(\#eq:bivalve4)
\end{equation}
</center>
<br>

where $Imax$ is maximum ingestion rate (mmol/mmol/d), $a_{I}$ is maximum standard ingestion rate (mmol/mmol/d), $W$ is weight (g), $bI$ is exponent for weight effect on ingestion, $L$ in length (mm) [@schneider1992; @bierman2005].
The temperature dependence function [@thornton1978] was fit to zebra and quagga mussel data (Hetherington et al. Submitted) with optimal ingestion from 17°C to 20°C according to the following:

<center>
<br>
\begin{equation}
f(T)_{I} = 1 \text{ for } T_{min_{I}} < T < T_{max_{I}}
(\#eq:bivalve5)
\end{equation}
</center>
<br>
<center>
\begin{equation}
f(T)_{I} = (2*\frac{Tmin_{TI}}{Tmin_{I}} - \frac{(Tmin_{TI})^2}{(Tmin_{I})^2}) / (2*\frac{Tmin_{I}-minT_{I}}{Tmin_{I}}-\frac{(Tmin_{I}-minT_{I})^2}{(Tmin_{I})^2}) \text{ for } minT_{I} < T < Tmin_{I}
(\#eq:bivalve6)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
f(T)_{I} = -\frac{(T^{2} + 2*Tmax_{I}*T–2*Tmax_{I}*maxT_{I} + maxT_{I}^{2})}{(Tmax_{I}-maxT_{I})^{2}}	\text{ for } Tmax_{I}<T<maxT_{I}
(\#eq:bivalve7)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
f(T)_{I} = 0	\text{ for } T > maxT_{I} \text{ or } T < minT_{I}
(\#eq:bivalve8)
\end{equation}
</center>
<br>

where $T$ is temperature (°C), $minT_{I}$ is lower temperature for no ingestion (°C), $Tmin_{I}$ is lower temperature for optimum ingestion (°C), $Tmax_{I}$ is upper temperature for optimum ingestion, $maxT_{I}$ is upper temperature for no ingestion (°C).
Filtration rate is related to food concentration [@walz1978; @sprung1988; @schneider1992; @bierman2005). The filtration rate is maintained at a maximum value for all food values less than saturation food concentration. The filtration rate decreases as food concentrations increase above this value.
Pseudofeces production is implicit as the difference between the mass filtered and consumed. According to @walz1978, pseudofeces production (66%) was approximately double the ingestion rate (34%) at high food concentrations @bierman2005.

Mussel density limits ingestion above some maximum density according to the following: 

<center>
<br>
\begin{equation}
$f(D) = 1$ 								     	     	for $D<Dmax$
(\#eq:bivalve9)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
f(D) = \frac{-(D^{2} + 2*Dmax*D – 2*Dmax*maxD + maxD^{2})}{(Dmax – maxD)^{2}} \text{ for } D>Dmax
(\#eq:bivalve10)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
f(D) = 0 \text{ for } D>maxD
(\#eq:bivalve11)
\end{equation}
</center>
<br>

where $D$ is density (mmol/m2), $Dmax$ is upper density for optimum ingestion (mmol/m2), and $maxD$ is upper density for no ingestion (mmol/m2).
An additional function to reduce ingestion is the suspended solids function which decreases ingestion with high inorganic loads according to the following:

<center>
<br>
\begin{equation}
f(SS) = 1 \text{ for } SS<SSmax
(\#eq:bivalve12)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
f(SS) = \frac{-(SS^{2} + 2*SSmax*SS – 2*SSmax*maxSS + maxSS^{2})}{(SSmax – maxSS)^{2}} \text{ for } SS>SSmax
(\#eq:bivalve13)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
f(SS) = 0 \text{ for } SS>maxSS
(\#eq:bivalve14)
\end{equation}
</center>
<br>

where $SS$ is suspended solids (mg/L), $SSmax$ is upper suspended solids for optimum ingestion (mg/L), and $maxSS$ is upper suspended solids for no ingestion (mg/L) [@spillman2008].
Along with suspended solids, salinity limits ingestion according to the following: 

<center>
<br>
\begin{equation}
f(S) = 1 \text{ for } Smin < S < Smax
(\#eq:bivalve15)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
f(S) = \frac{(2*(S-minS)/Smin)–(S-minS)^{2}/Smin^{2})}{(2*(Smin-minS)/Smin)–(Smin-minS)^{2}/Smin^{2})} \text{ for } minS< S < Smin
(\#eq:bivalve16)
\end{equation}
</center>
<br>
\begin{equation}
f(S) = \frac{-(S^{2} + 2*Smax*S – 2*Smax*maxS + maxS^{2})}{(Smax-maxS)^{2}} \text{ for } Smax<S<maxS
(\#eq:bivalve17)
\end{equation}
<center>
<br>
\begin{equation}
f(S) = 0 \text{ for } S > maxS \text{ or } S < minS
(\#eq:bivalve18)
\end{equation}
</center>
<br>

where $S$ is salinity (psu), $minS$ is lower salinity for no ingestion (psu), $Smin$ is lower salinity for optimum ingestion (psu), $Smax$ is upper salinity for optimum ingestion (psu), $maxS$ is upper salinity for no ingestion (psu) [@spillman2008].

#### Respiration {-}
Respiration is modelled as a base or standard respiration rate based on weight and temperature  [@spillman2008]. Respiration rate coefficient at 20°C is based on weight from length according to the following:

<center>
<br>
\begin{equation}
R_{20} = (a_{R} * W^{b}_{R})
(\#eq:bivalve19)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
W = \frac{0.071}{1000} * L^{2.8}
(\#eq:bivalve20)
\end{equation}
</center>
<br>

where $R_{20}$ is respiration rate coefficient at 20°C (mmol/mmol/d), $a_{R}$ is standard respiration rate (mmol/mmol/d), $W$ is weight (g), $b_{R}$ is exponent for weight effect of respiration, and $L$ is length (mm) (Schneider 1992).
The respiration rate coefficient is adjusted for temperature according to the following:

<center>
<br>
\begin{equation}
f(T)_{RSpillman} = \Theta_{RSpillman}^{T-20}
(\#eq:bivalve21)
\end{equation}
</center>
<br>

where $f(T)_{RSpillman}$ is respiration temperature function, $\Theta_{RSpillman}$ is temperature multiplier for bivalve respiration (-), and $T$ is temperature (°C) [@spillman2008].
Alternatively, respiration is modelled as a base or standard respiration rate based on weight and temperature in addition to the energetic cost of feeding. Respiration rate coefficient at 30°C is based on weight from length according to the following:

<center>
<br>
\begin{equation}
R_{30} = (a^{R} * W^{b}_{R})
(\#eq:bivalve22)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
W = \frac{0.071}{1000} * L^{2.8}
(\#eq:bivalve23)
\end{equation}
</center>
<br>

where $R_{30}$ is respiration rate coefficient at 30°C (mmol/mmol/d), $a^{R}$ is standard respiration rate (mmol/mmol/d), $W$ is weight (g), $b_{R}$ is exponent for weight effect of respiration, and $L$ is length (mm) [@schneider1992].
The temperature function follows @schneider1992 application of the model of @kitchell1977 to the data of @alexander_jr2004 according to the following:

<center>
<br>
\begin{equation}
f(T)_{RSchneider} = V^{X} * e^{X * (1-V)}
(\#eq:bivalve24)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
V = \frac{Tmax_{R} – T}{Tmax_{R} – maxT_{R}}
(\#eq:bivalve25)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
X = (\frac{W*(1+\sqrt{1 + (\frac{40}{Y})})}{20})^2
(\#eq:bivalve26)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
W = lnQ_{R}*(Tmax_{R} – maxT_{R})
(\#eq:bivalve27)
\end{equation}
</center>
<br>
<center>
<br>
\begin{equation}
Y = lnQ_{R}*(Tmax_{R} – maxT_{R} + 2)
(\#eq:bivalve28)
\end{equation}
</center>
<br>

where $T$ is temperature (°C), $Tmax_{R}$ is upper temperature for optimum respiration (°C), $maxT_{R}$ is upper temperature for no respiration (°C), and $Q_{R}$ is respiration curve slope estimate (-). The maximum respiration occurs at 30°C with 43°C as the upper lethal temperature.
The energetic cost of feeding or specific dynamic action is applied only to the portion of ingestion that is not egested [@schneider1992; @bierman2005; @gudimov2015].

#### Excretion {-}
Excretion is modelled as a constant fraction of assimilated food [@schneider1992; @bierman2005; @gudimov2015]. Excretion data for zebra and quagga mussels are limited; therefore, the excretion formulation for Mytilus edulis derived by Bayne and Newell (1983) was used [@schneider1992; @bierman2005; @gudimov2015].

#### Egestion {-}
Egestion is modeled as a function of ingestion [@schneider1992; @bierman2005; @gudimov2015]. The model follows the assumption that ingestion is directly proportional to the food content of the water for all food concentrations less than the maximum which can be ingested. For all food concentrations above this saturation value, ingestion remains constant at a maximum value ($I_{max}$) [@walz1978].

#### Mortality {-}
Mortality is a function of dissolved oxygen and predation (Equation 7). Mortality increases with low dissolved oxygen concentrations according to the following:

<center>
<br>
\begin{equation}
f(DO) = 1 + K_{BDO} * \frac{K_{DO}}{K_{DO} + DO}
(\#eq:bivalve29)
\end{equation}
</center>
<br>

where $DO$ is dissolved oxygen (mmol/m3), $K_{BDO}$ is basal respiration rate (mmol/m3), and $K_{DO}$ is half saturation constant for metabolic response to dissolved oxygen (mmol/m3) [@spillman2008]. A mortality rate coefficient ($K_{MORT}$) further influences the dissolved oxygen function. Additionally, mortality from predation is a constant rate added to the effect from dissolved oxygen.

###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<div id="refs"></div> 


<!--chapter:end:26-bivalves.Rmd-->

# Benthic Habitat Quality 

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:27-benthic_habitat_quality.Rmd-->

# (PART)  AED+ Riparian  Modules {-} 

# Soil Hydrology

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:28-soil_hydrology.Rmd-->

# Soil Biogeochemistry

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:29-soil_biogeochemistry.Rmd-->

# Acid Sulfate Soils

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:30-acid_sulphate_soils.Rmd-->

# Riparian Vegetation

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:31-riparian_vegetation.Rmd-->

# Riparian Habitat Quality

## Contributors
## Overview
## Model Description
###	Process Descriptions
###	Variable Summary
###	Parameter Summary
###	Optional Module Links
###	Feedbacks to the Host Model
## Setup & Configuration
## Case Studies & Examples
###	Case Study
###	Publications
## References

<!--chapter:end:32-riparian_habitat_quality.Rmd-->

# (PART)  Supporting Material {-} 

# Generic Utilities & Functions

## Overview


## Physico-chemical

### Gas Transfer

Target: review and select a few most popularly used gas exchange velocity to be used in AED modules. Note only key factors of wind speed, current speed, and water depths are considered. 

Selection criteria:

1. Environment: ocean; lake; estuary/river;
2. Study for which gas: O~2~, CH~4~, N~2~O, CO~2~
3. Variables: wind speeds ($U$), current speeds ($v$), depths ($h$)
4. Schmidt number normalization: yes/no. $Sc = \frac{\mu }{d} = \frac{\text{kinematic viscosity}}{\text{diffusion}}$


<center>
<div style="border: 1px solid #ddd; padding: 5px; overflow-y: scroll; height:500px; overflow-x: scroll; width:725px; "><table class="table table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:center;"> Source </th>
   <th style="text-align:center;"> Computation <br> $v$: current velocity <br> $U$: wind speed <br> $h$: water depth </th>
   <th style="text-align:center;"> Environment </th>
   <th style="text-align:center;"> Gas </th>
   <th style="text-align:center;"> Required Variables </th>
   <th style="text-align:center;"> $Sc$ Normalisation </th>
   <th style="text-align:center;"> Comment </th>
   <th style="text-align:center;"> AED Option Number </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;min-width: 12em; "> @liss1986 </td>
   <td style="text-align:center;min-width: 22em; "> $k = K_{600}(\frac{Sc}{600})^{-\frac{1}{2}}$ <br> $K_{600} = 0.17U$ for $U \leq 3.6$ <br> $K_{600} = 2.85U - 9.65$ for $3.6 \lt U \leq 13$ <br> $K_{600} = 5.9U - 49.3$ for $U \gt 13$ </td>
   <td style="text-align:center;"> Lake and ocean </td>
   <td style="text-align:center;"> CO~2~ </td>
   <td style="text-align:center;"> $U$ </td>
   <td style="text-align:center;"> Yes, 600 </td>
   <td style="text-align:center;min-width: 15em; "> One of the most popular formulas in early stage </td>
   <td style="text-align:center;"> $\Theta_{gas}^{schmidt} = 1$ </td>
  </tr>
  <tr>
   <td style="text-align:center;min-width: 12em; "> @wanninkhof1992 </td>
   <td style="text-align:center;min-width: 22em; "> $k = 0.31U^{2}(\frac{Sc}{660})^{-\frac{1}{2}}$ </td>
   <td style="text-align:center;"> Ocean, open lakes </td>
   <td style="text-align:center;"> CO~2~ </td>
   <td style="text-align:center;"> $U$ </td>
   <td style="text-align:center;"> Yes, 660 </td>
   <td style="text-align:center;min-width: 15em; "> One of the most globally popular formulas for oceans and lakes </td>
   <td style="text-align:center;"> $\Theta_{gas}^{schmidt} = 2$ </td>
  </tr>
  <tr>
   <td style="text-align:center;min-width: 12em; "> @wanninkhof2014 </td>
   <td style="text-align:center;min-width: 22em; "> $k = 0.251U^{2}(\frac{Sc}{660})^{-\frac{1}{2}}$ </td>
   <td style="text-align:center;"> Ocean, open lakes </td>
   <td style="text-align:center;"> CO~2~ </td>
   <td style="text-align:center;"> $U$ </td>
   <td style="text-align:center;"> Yes, 660 </td>
   <td style="text-align:center;min-width: 15em; "> Updated formula of @wanninkhof1992. Note the coefficient of 0.251 is now closer to @ho2011, @ho2016, and @borges2004. </td>
   <td style="text-align:center;"> $\Theta_{gas}^{schmidt} = 3$ </td>
  </tr>
  <tr>
   <td style="text-align:center;min-width: 12em; "> @ho2011 </td>
   <td style="text-align:center;min-width: 22em; "> $k = 0.26U^{2}(\frac{Sc}{600})^{-\frac{1}{2}}$ </td>
   <td style="text-align:center;"> Ocean, coastal area </td>
   <td style="text-align:center;"> He/SF~6~ </td>
   <td style="text-align:center;"> $U$ </td>
   <td style="text-align:center;"> Yes, 600 </td>
   <td style="text-align:center;min-width: 15em; "> Measurement at ocean and coastal area </td>
   <td style="text-align:center;"> $\Theta_{gas}^{schmidt} = 4$ </td>
  </tr>
  <tr>
   <td style="text-align:center;min-width: 12em; "> @ho2016 </td>
   <td style="text-align:center;min-width: 22em; "> $k = K_{600}(\frac{Sc}{600})^{-\frac{1}{2}}$ <br>  $K_{600} = 0.77v^{\frac{1}{2}}h^{-\frac{1}{2}}+0.266U^{2}$ </td>
   <td style="text-align:center;"> Estuary, rivers </td>
   <td style="text-align:center;"> He/SF~6~ </td>
   <td style="text-align:center;"> $v$,$U$,$h$ </td>
   <td style="text-align:center;"> Yes, 600 </td>
   <td style="text-align:center;min-width: 15em; "> Measurement at estuarine environment </td>
   <td style="text-align:center;"> $\Theta_{gas}^{schmidt} = 5$ </td>
  </tr>
  <tr>
   <td style="text-align:center;min-width: 12em; "> @raymond2001 </td>
   <td style="text-align:center;min-width: 22em; "> $k = K_{600}(\frac{Sc}{600})^{-\frac{1}{2}}$ <br> $K_{600} = 1.91exp(0.35U)$ </td>
   <td style="text-align:center;"> Estuary, rivers </td>
   <td style="text-align:center;"> CO~2~ </td>
   <td style="text-align:center;"> $U$ </td>
   <td style="text-align:center;"> Yes, 600 </td>
   <td style="text-align:center;min-width: 15em; "> An equation for estuary/river environment but against only on winds based on extensive review. Note the K value here is much higher than ocean environment in high wind speeds  (e.g. @wanninkhof1992). </td>
   <td style="text-align:center;"> $\Theta_{gas}^{schmidt} = 6$ </td>
  </tr>
  <tr>
   <td style="text-align:center;min-width: 12em; "> @borges2004 </td>
   <td style="text-align:center;min-width: 22em; "> $k = K_{600}(\frac{Sc}{600})^{-\frac{1}{2}}$ <br> $K_{600} = 1.0 + 1.719v^{\frac{1}{2}}h^{\frac{1}{2}}+2.85U$ </td>
   <td style="text-align:center;"> Scheldt Estuary </td>
   <td style="text-align:center;"> CO~2~ </td>
   <td style="text-align:center;"> $v$,$U$,$h$ </td>
   <td style="text-align:center;"> Yes, 600 </td>
   <td style="text-align:center;min-width: 15em; "> A equation for estuary environment from extensive measurement at Scheldt Estuary </td>
   <td style="text-align:center;"> $\Theta_{gas}^{schmidt} = 7$ </td>
  </tr>
  <tr>
   <td style="text-align:center;min-width: 12em; "> @rosentreter2016 </td>
   <td style="text-align:center;min-width: 22em; "> $k = K_{600}(\frac{Sc}{600})^{-\frac{1}{2}}$ <br> $K_{600CO_{2}} = -0.08+0.26v+0.83U+0.59h$ <br> $K_{600CO_{4}} = -1.07+0.36v+0.99U+0.87h$ </td>
   <td style="text-align:center;"> Estuaries </td>
   <td style="text-align:center;"> CO~2~, CH~4~ </td>
   <td style="text-align:center;"> $v$,$U$,$h$ </td>
   <td style="text-align:center;"> Yes, 600 </td>
   <td style="text-align:center;min-width: 15em; "> Equations developed specially for Queensland estuaries </td>
   <td style="text-align:center;"> $\Theta_{gas}^{schmidt} = 8$ </td>
  </tr>
</tbody>
</table></div>
</center>

## Biological

## References


<!--chapter:end:33-generic_utilities_functions.Rmd-->

# Publications

<!--chapter:end:34-publications.Rmd-->

# Abbreviations

<!--chapter:end:35-abbreviations.Rmd-->
