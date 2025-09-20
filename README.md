# Virtual_Screening

 Project Workflow (step-by-step)
 
	1.	Upload receptor (PDBQT) & ligands (CSV)
 
	•	Upload your target protein structure (target.pdbqt).
 
	•	Upload your ligand library (library.smi, ~500 ligands csv format).
 
	2.	Protein preparation
 
	•	Cleaning of protein was done in ChimeraX , removed water, co-crystalized  ligand , fix missing atoms/residues, and added hydrogens, charges then saved as protein_cleaned.pdb
 
	•	Convert to .pdbqt in Pyrx for autodock.
 
	3.	Ligand preparation
 
	•	Read .csv file.
 
	•	Generate 3D conformations with RDKit.
 
	•	Energy minimize (UFF).
 
	•	Convert to .pdbqt using OpenBabel.
 
	4.	Docking with AutoDock Vina
 
	•	Defined binding site box (use centroid of active site or co-crystallized ligand).
 
	•	Docked each ligand against the protein.
 
	•	Collected binding affinities (kcal/mol).
 
	5.	Post-processing and Virtual_screening
 
	•	Rank ligands by docking score (more negative = better).
 
	•	Applied Lipinski’s Rule of 5 filters (MW, LogP, HBD, HBA).
 
	•	Save results to CSV (top_hits.csv).
