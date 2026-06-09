# Electric Field Redistribution Driven SEGR Mitigation in a High-k Trench VDMOS with Floating Islands

## Manuscript Information

**Title:** Electric Field Redistribution Driven SEGR Mitigation in a High-k Trench VDMOS with Floating Islands

**Manuscript ID:** IEEE Latin America Transactions – ID: 10555

### Authors

**Sanjeev Manoj Ranjan**
Department of Electronics and Communication Engineering
National Institute of Technology Raipur, India

**Saikat Majumder**
Department of Electronics and Communication Engineering
National Institute of Technology Raipur, India

**Alok Naugarhiya**
Department of Electronics and Communication Engineering
National Institute of Technology Raipur, India

---

## Repository Purpose

This repository accompanies the manuscript **"Electric Field Redistribution Driven SEGR Mitigation in a High-k Trench VDMOS with Floating Islands."**

The repository provides all TCAD simulation decks, mesh definitions, heavy-ion irradiation setups, datasets, and figures required to reproduce the reported electrical and radiation-hardness results presented in IEEE Latin America Transactions Manuscript ID 10555.

---

## Software Requirements

The simulations were performed using:

* Silvaco Atlas
* Silvaco Athena
* Silvaco Victory Process
* Silvaco Victory Device
* Silvaco Victory Mesh
* TonyPlot

**Software Version:** Silvaco TCAD Version 5.28.1.R

---

## Repository Structure

### 01_Device_Structure/

Contains the complete TCAD structure-definition files used to generate the conventional trench VDMOS and the proposed high-k + PFI VDMOS architectures. These files define the device geometry, material regions, electrodes, and doping profiles used throughout the study. The generated structures serve as the starting point for all subsequent simulations.

### 02_Mesh_Files/

Contains mesh-generation and remeshing scripts used to improve numerical accuracy in critical regions such as the trench oxide interfaces, trench neck, drift region, and floating-island structures. The mesh settings were optimized to ensure reliable electric-field extraction, breakdown analysis, and transient heavy-ion simulations.

### 03_Static_Simulations/

Contains simulation decks used for static electrical characterization of the devices. These include threshold voltage (Vth), breakdown voltage (BV), specific on-resistance (Ron,sp), transfer characteristics, and electric-field distribution analyses. Extraction commands required to reproduce the reported results are embedded within the corresponding simulation files.

### 04_Heavy_Ion_SEGR/

Contains simulation inputs associated with heavy-ion irradiation and single-event gate rupture (SEGR) investigations. The files include heavy-ion strike definitions, linear energy transfer (LET) configurations, transient simulation setups, and oxide electric-field extraction procedures used to evaluate radiation-induced degradation mechanisms.

### 05_Data/

Contains both raw and processed datasets (.csv) generated during the simulation campaign. Raw data include simulation output logs and transient responses, while processed data contain extracted values used for figures and manuscript preparation.

### 06_Figures/

Contains exported figures and graphical assets used in the manuscript. This includes device schematics, electric-field contour plots, and transient-response plots. The figures are provided to facilitate result verification and manuscript reproducibility.

---

## Repository Contents and Corresponding Manuscript Results

The repository contains all simulation input files, datasets, and graphical outputs required to reproduce the simulation results presented in the manuscript.

| Code / Script / Model                                                                                                                                         | Folder Name                                                                              | Related Figure(s)              | Description                                                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| ConventionalDevice.in, ProposedDevice (TrenchVDMOSwithHigh-kandFloatingIslands).in                                                                            | 01_Device_Structure, 02_Mesh_Files                                                       | Fig. 2, Fig. 3                 | Conventional and proposed device structures with mesh refinement.                                                                                   |
| TCADCalibration.in                                                                                                                                            | 03_Static_Simulations/Calibration_of_TCAD_Simulation_Framework                           | Fig. 6                         | Calibration of the TCAD simulation framework.                                                                                                       |
| ConventionalDevice_BV.in, ProposedDevice(TrenchVDMOSwithHigh-kandFloatingIslands)_BV.in                                                                       | 03_Static_Simulations/ProposedDevice                                                     | Fig. 7                         | Breakdown voltage and electric-field variation versus PFI concentration in the proposed structure.                                                  |
| Conv_ElectricContour.in, Proposed_ElectricContour.in, ConventionalDevice_FieldLines.in, ProposedDevice(TrenchVDMOSwithHigh-kandFloatingIslands)_FieldLines.in | 03_Static_Simulations/ElectricFieldContours, 03_Static_Simulations/FieldLineDistribution | Fig. 8(a-d), Fig. 9(a-d)       | Electric-field contour and field-line distributions for conventional, high-k, PFI, and proposed high-k + PFI VDMOS structures.                      |
| LengthVaryPositionDopingSame.in, VaryPositionofFLI.in, RON_PFI_2.in, RON_PFI_3.in, RON_PFI_4.in                                                               | 03_Static_Simulations/ConventionalDevice, 03_Static_Simulations/ProposedDevice           | Fig. 10–17                     | Breakdown voltage, electric-field variation versus PFI length, position, concentration, and specific on-resistance variation versus number of PFIs. |
| Conv_LET20.in, Conv_LET37.in, Conv_LET40.in, Prop_LET20.in, Prop_LET37.in, Prop_LET40.in                                                                      | 04_Heavy_Ion_SEGR/conventional, 04_Heavy_Ion_SEGR/proposed                               | Fig. 18, Fig. 19, Fig. 20(a-f) | Transient heavy-ion response of conventional and proposed structures under LET = 20, 37, and 40 MeV·cm²/mg.                                         |

---

## Reproducibility Workflow

The following workflow should be followed to reproduce the simulation results reported in the manuscript:

1. Generate device structures.
2. Perform mesh generation and refinement.
3. Run static electrical simulations.
4. Run heavy-ion transient simulations.
5. Extract results and reproduce manuscript figures.

---

## Contact

For questions regarding repository contents, simulation setup, or result reproducibility, please contact the corresponding author.
