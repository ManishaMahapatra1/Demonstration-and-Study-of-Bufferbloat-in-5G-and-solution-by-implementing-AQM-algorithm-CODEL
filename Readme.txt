Code Files:	
	** The required code files are present in the Codes folder in the zipped folder **	
	
	Phase 1:
		1) The project_task1.cc file must be present in the scratch folder to be run.
		2) It can be run with the command:
			./ns3 run project_task1.cc
		3) To modify the lambda values for the respective flows you will have to manually adjust the values in line number 422 and line 433.
		   With 422 for the mice flow ( flow 1) and 433 for the elephant flow ( flow 2 ).
		4) The Output flowstats are printed in the file with the name indicated by simTag variable on line 110.
		5) To generate the pcap for the respective simulation please uncomment the code present in line 477.( pcap generated with name 'resuts').
		6) To generate the respective RLC log files ensure that you uncomment the code on line 86  to enable logging and use the command
			./ns3 run "project_task1.cc"&>RLC_log.txt		 

	Phase 2 :
		1) Varying the RLC buffersize:
			-> We vary the RLC buffer by manually by adjusting the code on the line 199 ( declaring the buffer size ).
		2) CoDel Implementation:
			-> To run the CoDel implementation the lte-rlc-um.cc file present in the src/lte/model folder must be replace with the file give in the tar.gz ball.
			-> Once the File has been replace we can manually set the threshold and interval times in the lte-rlc-um.cc for the codel algorithm by modifying the respective 
			   global variables in them.
			-> We can then run the Phase 1 simulation same as in the above steps and observe the results in the respective outputs.
			-> To disable the CoDel procedure either revert back to the old lte-rlc-um.cc or comment out the return commands present in lines 114 and 120.
			
			
	***
	All graphs have been generated using online tools after extracting the data by the running the code the required number of times.
	*** 

Output Files:
	1) The respective output files for the phase 1 ( Vanilla Implementation ) and both phase 2 implementations ( RLC buffer size variation and CoDel implmentation) are present 
	in the Outputs folder of the zipped folder.
	2) The readings of the output files for the Vanilla and Codel Implementation are present in ascending order of lambda2 ( 15000,20000,25000...).
	3) The readings of the output file for the RLC buffer size variation are present in desceding order of buffer size ( 10*10^7, 9*10^7,...).
	4) Pcap output for the phase 1 implementation is present in the outputs folder.
	5) RLC logs generated for phase 1 is stored in the output folder.
	
