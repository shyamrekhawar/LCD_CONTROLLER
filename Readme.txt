########################################################
This is Read Me file

#######################################################
/***************************************************************************************************************************************
* PROJECT NAME: LCD CONTROLLER TESTBENCH     DATE:12/01/2017
* CREATED BY: SARVESH DATAR, SHYAM REKHAWAR, MANC WARDE
* DESCRIPTION: THIS TESTBENCH ACTS AS MEMORY MODULE FOR THE DUT AND ALSO AS MASTER FOR LADING THE CONFIGURATION REGISTERS OF THE DUT
*              THE TESTBENCH CHECKS THE FUNCTIONALITY OF LCD CONTROLLER.
***************************************************************************************************************************************/
WHAT PASSED / WHAT DID NOT:
	In the Project, DUT0/LCD0  passes for all the test cases.

	DUT1/LCD1 passes for testcase t0-t3 and t12-t15 and fails for t4-t11

	DUT2/LCD2 fails for all the test cases.

	DUT3/LCD3 fails for all testcases due to Vertical Sync pulse failure.
FILES:
	tblcd.sv:
		Contains the top level module.
	lcduvm.svp:
		It contains driver1,monitor1 and scoreboard. Driver1 sends the signals when DUT acts as Master. Monitor 1 captures the LCDOUT data at LCDCLK.
	lcduvm2.svp:
		It contains driver2,monitor2. Driver2 sends the signals when DUT acts as SLAVE. Monitor2 collects HCLK for Vertical sync check.
COMAND:
	./sv_uvm tblcd.sv

OUTPUT FILES:
	Error.txt:
		Indicates the Error checking
	Error_file.txt:
		Shows which test sequence failed.
	result[0-15].txt
		Shows the simulation results. It shows the comparison between the Expected output and Output from DUT.

FOLDERS:
	lcd[0-3]_sim_result:
		Contains the simulation result for DUT0-DUT1-DUT2-DUT3 in files result[0-15].txt and Error_file.txt file shows which test sequence failed for that particular dut. Error.txt contains the Errors from simulation.


