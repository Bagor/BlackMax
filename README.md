# LHEreaderBM

You can take actual version of BlackMax generator from
https://blackmax.hepforge.org/downloads/

For example:

mkdir BlackMax
cd BlackMax
wget https://blackmax.hepforge.org/downloads/BlackMax-2.02.0.tar.gz
gunzip BlackMax-2.02.0.tar.gz
tar -xvf BlackMax-2.02.0.tar

in Make file
PDFLIB = /afs/cern.ch/sw/lcg/external/MCGenerators/lhapdf/5.8.9/x86_64-slc5-gcc43-opt/lib/

Also, you can swtich off gcc parameters to use the last version of gcc:
#COMP    = -fno-globals -fno-automatic -finit-local-zero

gmake BlackMax
./BlackMax

Ensure that your LD_LIBRARY_PATH environment variable includes the location
of your newly built LHAPDF library, etc:

setenv LD_LIBRARY_PATH /usr/lib/gcc/x86_64-redhat-linux6E/4.4.6/:/afs/cern.ch/sw/lcg/external/MCGenerators/lhapdf/5.8.9/x86_64-slc5-gcc43-opt/lib
setenv LHAPATH /afs/.cern.ch/sw/lcg/external/MCGenerators/lhapdf/5.8.9/share/PDFsets

