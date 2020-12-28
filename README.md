# Play-data-MD
COLVAR_data: Provides time-series data for each chi1 and chi2 angle  (Main file)

COLVAR_sincos: Time-series data with sin and cos modifications of each chi1 and chi2 angles respectively.

scaledfeatures.pkl: Output of scaled_feature.py (run: python scaled_feature.py) which consists of scaled sin and cos modifications of each chi1 and chi2 angles.

Download the data here: https://www.dropbox.com/s/7sb8sg7at0icu7h/data.zip?dl=0

In order to reproduce vde-res-75-86.ipynb you need the .pkl files which can be found here https://www.dropbox.com/sh/uxzgmomldcc3gxa/AAAjlLpwgE-_-pnPRqjKn4Tia?dl=0

In order to run .py files you need:

1. Python 3.6
2. MSMBuilder: http://msmbuilder.org/3.8.0/
3. MDTraj: https://mdtraj.org/1.9.4/index.html 
4. Pandas
5. Numpy
6. VDE https://github.com/msmbuilder/vde 

You can see a movie of how the protein fluctuates. Install VMD in your computer and then type the following:

vmd prot.pdb trajfit.xtc 

trajfit.xtc is a big file. Please contact the author to get the file seperately.

Removing periodicity from data: sin(x)-<mean> or cos(x)-<mean>
 
 Notes:
 
 Plumed.dat file produces the COLVAR files:

You need to install Plumed in your computer and then run: 

Plumed driver --mf_xtc trajfit.xtc --plumed plumed.dat --pdb prot.pdb

Please email bhakatsoumendranath@gmail.com for more details
