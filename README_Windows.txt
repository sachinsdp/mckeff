!*************************************************************************
!***  README.txt  ***
!*************************************************************************
!
!    Contents

	A.Test Run of MCkeff
	B.MCkeff DVD folder’s information
	C.Cross section configuration

!************************************************************************************

A. Test Run of MCkeff

	1. User Computer with windows 7 or later

	2. Copy the folder "test_run" to your computer

	3. Open Command prompt [Press "Windows+R" , then type "cmd" and press "enter"]

	4. Change the path to the copied folder "test_run". [eg., cd c:\user\test_run].

	5. Type "mckeff" and press "enter" to run a the sample input.

	   This will create sample output file named, "out1".

	6. To get the Geometry plot of the input, type "mckeff -p" and press "enter"


	If the above procedure is succesfuly completed, Copy the all the DVD contents
	to a folder say, MCKEFF, and do the cross_section 
	configuration(Next-steps) to run any other input problems.
 

!************************************************************************************

B. MCkeff DVD folder’s information

	The distribution DVD contains  MCkeff source code modules, 
	cross sections documentation and result are  in a DVD.
	The folder and the respective information of the DVD are as given below.

	!_________________________________________________________________________
	1. > MCKEFF/Documents/ 
	   mckeff.pdf contains full documentation of the code
	
	!_________________________________________________________________________
	2. > MCKEFF/Source_Code/ 
	
	    This folder contains Fortran source code files (*.F90) 
	    MAKEFILE.WINDOWS and MAKEFILE.LINUX
	    These are makefiles to compile and create executable files
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
	     zip files. The files are ENDF-B-VII.1-neutron-300K.zip.
	     These data files can also be downloaded from the following site.
	     https://www.nndc.bnl.gov/endf/b7.1/acefiles.html
	 
	!_________________________________________________________________________
	5. > MCKEFF/Compilers/
	
	     Windows: The GNU distributed windows gcc compiler. The same compiler
	     can be downloaded from the site http://www.equation.com 
	
	!_________________________________________________________________________
	6. > MCKEFF/Developing_Tools/
	
	    This folder contains IDE(Codeblocks) and MCkeff codeblock project files. 
	    Copy this folder and open the mckeff.cbp file with Codeblocks.
	!_________________________________________________________________________


!*******************************************************************************

C. Cross section configuration

	1. The required cross section files are given in the folder "MCKEFF\cross_sections". 

	2. Extract the zip file "ENDF-B-VII.1-neutron-300K.zip" to a folder say "endf_cxs". 

	3. Locate and move the file "xsdir" from folder "endf_cxs"  to the "mckeff" executables directory.

	4. Copy the path to the folder "endf_cxs" [eg.,copy the text "C:\user\xyz\endf_cxs"]

	5. Edit the first line of the file "xsdir" as below:


		datapath=C:\user\xyz\endf_cxs


	6. Now cross sections are configured. Run any other input files


!*******************************************************************************

 ***   Refer to mckeff.pdf for building the mckeff executable from source  ***

!*******************************************************************************
!For help Contact: 
	K.V.Subbaiah [kv.subbaiah@manipal.edu]
        Sachin Shet  [iamsachinshet@gmail.com][+91-8971237086]


