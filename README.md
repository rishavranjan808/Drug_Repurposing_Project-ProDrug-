# Drug_Repurposing_Project
This project provides a comprehensive tool for predicting gastrointestinal absorption (GIA) and blood-brain barrier (BBB) penetration based on molecular properties derived from the BOILED-Egg model. The project is implemented in Python and uses RDKit for cheminformatics and Shapely for geometric analysis.


## Project Overview
The BOILED-Egg model, developed by Daina and Zoete in 2016, is a widely recognized method for predicting the absorption and distribution of drugs within the human body based on molecular properties. This tool allows users to upload molecular structure data files in .sdf format, process the molecular data, and output predictions of GIA and BBB penetration.

## Key Features
### Molecular Descriptor Calculation:

Topological Polar Surface Area (TPSA): Calculated using RDKit's Descriptors.TPSA, considering the contributions from sulfur and phosphorus atoms.
Wildman and Crippen LogP (WLogP): Representing molecular lipophilicity, also calculated using RDKit.
### Geometrical Analysis:

The tool defines specific regions in the TPSA vs WLogP space as ellipses, representing areas where molecules are likely to exhibit good GIA or BBB penetration.
These regions are defined using the Polygon class from shapely. geometry.
### Data Handling:

Users can upload multiple .sdf files, each containing a series of molecular structures.
For each molecule, TPSA and WLogP are calculated, and it is determined whether the molecule falls within the predefined GIA or BBB regions.
### Output:

A CSV file summarizing the molecular properties and their classification concerning GIA/BBB regions.
A scatter plot visualizing the TPSA-WLogP space, with the GIA and BBB regions overlaid. The plot is saved as both PDF and PNG files.
