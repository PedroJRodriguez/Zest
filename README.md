# Zest board design
The board is designed in KiCAD 8.0. 

git clone https://gitlab.com/lbl-boards/zest

Open the design: 
From KiCAD GUI:
File->Open Project...
and nevigate the project file: zest.kicad_pro 
From command line
kicad zest.kicad_pro

Generate fabrication package
make fab
It will download a script I had in the BIDS repo and use it. I didn't include the whole BIDS as submodule because I don't feel it's necessary, as I am only using this single file here. 

Generate QR code for SN 
Make sure the gerber.py already exist in the scripts directory, if not, run make gerber.py and it will download from the BIDS repo.
python qrsn.py zest -start 10 -stop 20
This will generate the gerber file for the 10 different SN.

I can not include the footprint files because many of them were downloaded from digikey.com or snapeda.com.