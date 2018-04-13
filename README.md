# flavin_fun
# Getting Started with Flavin Fun

Programs Needed to Run Files
-------
To properly get all the scripts to run you must have the following programs and packages: 
  * Python 3 
  * Jupyter Notebook 
  * Anaconda Navigator 
  * BioPandas
  * NumPy (1.11.2) 
  * SciPy (0.18.1)
  * Pandas (0.19.1) 

How to Install Programs
-------
(1) Install Python 3: To install, follow the steps from https://www.python.org/downloads/ according to your operating system.

(2) Download Anaconda Navigator: To install, go to https://docs.anaconda.com/anaconda/navigator/ and click 'Install Anaconda' under the "What is Anaconda Navigator" paragraph. Follow the steps on the following page according to your operating system. 

Once Programs are Installed
-------
(1) Clone Github Repository flavin_fun (https://github.com/FlavoInformatics/flavin_fun) and pull the files onto your local drive. 
If unsure how to clone repository and pull github files, please reference https://help.github.com/articles/cloning-a-repository/.

(2) Once files are successfully on your local drive, open Anaconda Navigator and launch Jupyter Notebook from the Home tab. 

(3) After selecting Jupyter Notebook, locate the files on your local drive.

(4) Depending on which flavoprotein analysis wanted, open the corresponding file in Jupyter Notebook. (Please see flavin_fun file outline below) 

Outline of Files in flavin_fun Repository 
-------
1. **atom_type_count.ipynb** - Outputs the frequency of chemical types surrounding the whole isoalloxazine structure in the flavoprotein and, more specifically, the frequency of chemical types surrounding individual atoms within the isoalloxazine.

2. **cluster.ipynb**- First, finds the frequency of chemical types surrounding the whole isoalloxazine structure in each flavoprotein. A k-means clustering analysis is run on all the flavoproteins based frequency of the chemical types found in the first step and a CSV file is generated that contains the frequency of chemical types surrounding the isoalloxazine structure for each flavoprotein and which k-means clustering group the flavoprotein belongs in. *this file can only be run if the user downloads all Protein Database FMN and FAD flavoprotein molecules

3. **code.csv**- Contains the chemical code mapping associated with the atoms and their residues. 

4. **code_labels.csv**- Contains the chemical label associated with the chemical code. 

5. **distances.ipynb**- Outputs CSV file of distance between reference atoms, isoalloxazine in flavoprotein specificied by user, and surrounding atoms in Ångström range specified by user. 

6. **pdb_codes.txt**- Contains all FMN and FAD flavoprotein molecules on the Protein Data Bank (Updated as of April 10, 2018).

Tradeoffs 
-------
1. Data is acquired from the Protein Data Bank, any errors in flavoprotein information may be due to PDB standards.
2. Clustering tool is only functional with use of the local USB drive.
3. New flavoprotein molecules must be downloaded onto the USB drive in the FlavinTest folder.
