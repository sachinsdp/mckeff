!*************************************************************************
!***  README.txt  ***!
!*************************************************************************

	Contents

	A. MCkeff DVD folder’s information.
	B. Installing steps for "mckeff".
	C. Cross section configuration.


!**************************************************************************
A. MCkeff DVD folder’s information

	The distribution DVD contains  MCkeff source code modules, 
	cross sections documentation and result are  in a DVD.
	The folder and the respective information of the DVD are as given below.

	1. > MCKEFF/Documents/ 
	   mckeff.pdf contains full documentation of the code
	
	!_________________________________________________________________________
	2. > MCKEFF/Source_Code/ 
	
	    This foldercontains Fortran source code files (*.F90) 
	    MAKEFILE.WINDOWS and MAKEFILE.LINUX
	    These are batch files to compile and create executable files
	    under 2 different Operating Systems.
	
	!_________________________________________________________________________
	3. > MCKEFF/Inputs_Outputs/
	
	     This folder contains sub-folders namely inputs and outputs.
	     Each contains several test input and output files for MCkeff,MCNP5,OPenMC codes 
	     MCNP and MCkeff input files are given a serial file names as “inp0n”
	     OpenMC files are given as a separate folder named input_OpenMC
	     The MCNP, MCkeff and OpenMC output files are prefixed with letters M, K , and O
	     respectively which can be found in the folder OUTPUTS. 
	     Comparison of results among the codes given in Chapter-6 in MCKEFF>Documents 
	!_________________________________________________________________________
	4. > MCKEFF/Cross_Sections/
	
	     This folder contains ACE fomatted continuous energy neutron cross section
	     zip files. The files are ENDF-B-VII.1-neutron-300K.zip
	     These data files can be downloaded from the following site.
	     https://www.nndc.bnl.gov/endf/b7.1/acefiles.html
	 
	!_________________________________________________________________________
	5. > MCKEFF/Compilers/
	
	     Windows: The GNU distributed windows gcc compiler. The same compiler
	     can be downloaded from the site http://www.equation.com 
	     Linux: The GNU distributed compiler can be installed with the command
	            sudo apt install gfortran make on UBUNTU 19.04 LTS.
	
	!_________________________________________________________________________
	6. > MCKEFF/Developing_Tools/
	
	    This folder contains IDE(Codeblocks) and MCkeff codeblock project files. 
	    Copy this folder and open the mckeff.cbp file with Codeblocks.
	!_________________________________________________________________________	


!*************************************************************************

B. Installing steps for "mckeff"

	This procedure tested under UBUNTU 19.04 LTS
	_________________________________________________________________________

	1. Copy all the data from DVD to your Computer to a folder Say, MCKEFF.

	2. Run command "sudo apt install gfortran make" to install pre-requisites

	3. Open Command window (Open Terminal)

	4. Change directory to "MCKEFF/source_code" folder

	5. Run the command "make -f makefile.linux" 
	
	    ***Now we have mckeff executable in the folder***

	6. Run "mckeff" executable [eg., ./mckeff]

	7. Configure cross_section(next-step) to run other problem

!*******************************************************************************

C. Cross section configuration

	1. The required cross section files are given in the folder "MCKEFF/cross_sections". 

	2. Extract the zip file "ENDF-B-VII.1-neutron-300K.zip" to a folder say "endf_cxs". 

	3. Locate and move the file "xsdir" from folder "endf_cxs"  to the "mckeff" executables directory.

	4. Copy the path to the folder "endf_cxs" [eg.,copy the text "usr/docs/endf_cxs"]

	5. Edit the first line of the file "xsdir" as below:


		datapath=usr/docs/endf_cxs


	6. Now cross sections are configured. Run any other input files

!********************************************************************************
!For help Contact: 
	K.V.Subbaiah [kv.subbaiah@manipal.edu]
        Sachin Shet  [iamsachinshet@gmail.com][+91-8971237086]
