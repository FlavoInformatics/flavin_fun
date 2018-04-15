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

(3) Download Python Modules (i.e. BioPandas, Pandas, etc.): Fortunately, Anaconda Navigator will download Pandas, NumPy, and SciPy by default. Only BioPandas is missing. To download BioPandas:
 - **Mac**: To install, open Terminal on the Mac (this can be done easily by searching "Terminal" on the Mac's spotlight search. In the terminal, type **conda install -c conda-forge *insert_module***.
   - To download BioPandas, type **conda install -c conda-forge biopandas** in the Terminal.

Once Programs are Installed
-------
(1) Clone Github Repository flavin_fun (https://github.com/FlavoInformatics/flavin_fun) and pull the files onto your local drive. 
If unsure how to clone repository and pull github files, please reference https://help.github.com/articles/cloning-a-repository/.

(2) Once files are successfully on your local drive, open Anaconda Navigator and launch Jupyter Notebook from the Home tab. 

(3) After selecting Jupyter Notebook, locate the files on your local drive.

(4) Depending on which flavoprotein analysis wanted, open the corresponding file in Jupyter Notebook. (Please see flavin_fun file outline below) 

**Editing BioPandas Module**
-------
(1) Editing BioPandas: BioPandas needs to be slightly modified to be able to read biological assemblies.
  - **Mac**: 
    - Open up the "pandas_pdb.py" file that was downloaded from the previous step. 
    - Highlight the whole code and copy it.
    - To edit the BioPandas to fit our needs, search **biopandas** on spotlight search and choose the folder "biopandas". After choosing biopandas, go into the **pdb** folder. Choose the "pandas_pdb.py" file. 
    - Select all and replace the code with the code that was copied in the previous step.
    - Save the file.
    - Restart Anaconda Navigator.

Outline of Files in flavin_fun Repository 
-------

**Note: Make sure all files are in the same folder/directory**

1. **distances.ipynb**- Outputs CSV file of distance between reference atoms, isoalloxazine in flavoprotein specificied by user, and surrounding atoms in Ångström range specified by user. 

2. **chemical_type_count.ipynb** - Outputs the frequency of chemical types surrounding the whole isoalloxazine structure in the flavoprotein and, more specifically, the frequency of chemical types surrounding individual atoms within the isoalloxazine.

3. **cluster.ipynb**- First, finds the frequency of chemical types surrounding the whole isoalloxazine structure in each flavoprotein. A k-means clustering analysis is run on all the flavoproteins based frequency of the chemical types found in the first step and a CSV file is generated that contains the frequency of chemical types surrounding the isoalloxazine structure for each flavoprotein and which k-means clustering group the flavoprotein belongs in. This will take a long time, depending on how many flavoproteins you are analyzing. 

4. **clustering_add_on.ipynb** Allows the user to update the CSV file created from the "cluster.ipynb" by appending new flavoproteins. The purpose of this script is to allow users to add new flavoproteins and run the K-means clustering on all the flavoproteins again while not having to run through every single flavoprotein.

5. **cluster_dataframe.ipynb** Allows the user to display specified clusters from the CSV file. If the user wants to see the flavoproteins in cluster 1, then this script allows this.

6. **code.csv**- Contains the chemical code mapping associated with the atoms and their residues. 

7. **code_labels.csv**- Contains the chemical label associated with the chemical code. 

8. **pdb_codes.txt**- Contains all FMN and FAD flavoprotein molecules on the Protein Data Bank (Updated as of April 10, 2018).

Tradeoffs 
-------
1. Data is acquired from the Protein Data Bank, any errors in flavoprotein information may be due to PDB standards.
2. Clustering tool is only functional with use of the local USB drive.
3. New flavoprotein molecules must be downloaded onto the USB drive in the FlavinTest folder.
