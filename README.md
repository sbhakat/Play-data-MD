# Play-data-MD
COLVAR_data: Provides time-series data for each chi1 and chi2 angle  (Main file)

COLVAR_sincos: Time-series data with sin and cos modifications (Removing periodicity from data: sin(x)-mean or cos(x)-mean where x is chi1 or chi 2 angles) of each chi1 and chi2 angles respectively.(Main file)

scaledfeatures.pkl: Output of scaled_feature.py (run: python scaled_feature.py) which consists of scaled sin and cos modifications of each chi1 and chi2 angles. (Same as COLVAR_sincos but in .pkl format)

Download the data here: https://www.dropbox.com/s/7sb8sg7at0icu7h/data.zip?dl=0

In order to reproduce vde-res-75-86.ipynb you need the .pkl files which can be found here https://www.dropbox.com/sh/uxzgmomldcc3gxa/AAAjlLpwgE-_-pnPRqjKn4Tia?dl=0

In order to run .py files you need:

1. Python 3.6
2. MSMBuilder: http://msmbuilder.org/3.8.0/
3. MDTraj: https://mdtraj.org/1.9.4/index.html 
4. Pandas
5. Numpy
6. VDE https://github.com/msmbuilder/vde 

Presentation can be found here: https://www.dropbox.com/s/xznpqom927sv5xk/data-competition.key?dl=0 

For Curious folks:

You can see a movie of how the protein fluctuates. Install VMD in your computer and then type the following:

vmd prot.pdb trajfit.xtc 

trajfit.xtc is a big file. Please contact the author to get the file seperately.

For more information on this dataset read our paper:
https://www.biorxiv.org/content/10.1101/2020.04.27.062539v1

Interesting papers on ML in context of molecular dynamics simulation:
1. Machine learning approaches for analyzing and enhancing molecular dynamics simulations, https://www.sciencedirect.com/science/article/abs/pii/S0959440X19301551
2. Machine Learning for Molecular Simulation, https://www.annualreviews.org/doi/abs/10.1146/annurev-physchem-042018-052331
3. Learning molecular dynamics with simple language model built upon long short-term memory neural network, https://www.nature.com/articles/s41467-020-18959-8

 
 Notes:
 
 plumed.dat file produces the COLVAR files:

You need to install Plumed in your computer and then run: 

plumed driver --mf_xtc trajfit.xtc --plumed plumed.dat --pdb prot-plm-apo.pdb

Please email bhakatsoumendranath@gmail.com for more details
