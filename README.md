# RSV_model
Age-structured model of RSV transmission, calibrated to laboratory-confirmed RSV hospitalisations data for Western Australia.

The model was previously coded in MATLAB and is fully described in this publication: https://www.sciencedirect.com/science/article/pii/S0264410X17312720?via%3Dihub. The model is now coded in R, and the 'baseline' model (without vaccination) is provided in this repository.

Briefly, the model is a system of ordinary differential equations, compartmentalised as Susceptible-Exposed-Infectious-Recovered-Susceptible, and further stratified into 75 age compartments: 60 one-month compartments up to 5 years of age, and 5-year groups thereafter. The contact structure is informed by the POLYMOD study. Ageing in the model is implemented by cohort ageing (where the initial conditions are manually updated each month). The ordinary differential equations are solved using the odin package (https://github.com/mrc-ide/odin).
