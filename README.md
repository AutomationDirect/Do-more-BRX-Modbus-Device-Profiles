# Do-more BRX Modbus Device Profiles
Repository for Modbus Device Profiles

Do-more Designer 2.9.0 introduced the Modbus Scanner. BRX CPUs can use a Modbus I/O Scanner to process Modbus Read and Modbus Write requests similarly to the way it handles local I/O and Ethernet Remote I/O. It does this by creating a Scanner Device for any combination of up to 32 Modbus/TCP or Modbus/RTU servers. The Scanner Device can additionally perform any required format conversion on the data, removing the need to add ladder logic to process the data before it is sent or after it is received.
The Modbus I/O Scanner processes communication requests for up to 32 Scanner Devices, each of which uses a Modbus/RTU or Modbus/TCP Client device to communicate with a target Modbus Server. Scanner Devices can be created using the following two methods: 


1. Using a profile that was created for a specific Modbus Server. 

A profile defines the Modbus Reads and Writes that will be processed, where the data for these Reads and Write are sourced from or stored to as appropriate, and any byte-swapping / word-swapping or scaling that may be needed as part of the Read or Write operation. A profile can be built so that it uses either a user-defined data structure or built-in memory blocks for storing the Scanner Device's data.  
  * There are system profiles (*.mdp) that are provided with the Do-more Designer software for many of the Modbus Server devices that are sold by Automationdirect.com. Scanner Devices built with a system profile will have a fixed configuration that cannot be altered to include additional comm requests, or delete existing comm requests, or change the PLC memory storage configuration. 
  * There are also user profiles (*.mup) that are built by the Scanner Device configuration utility from the Modbus Read, Modbus Write, and mapping information supplied by the user when the Scanner Device is created.


* Starting with a blank device which has no predefined communication requests, and manually adding the required Modbus Read requests, Modbus Write requests, and the associated mapping for PLC data storage locations for the Modbus Server. Once a blank Scanner Device has been created, the configuration of that device can be used to build a user profile (*.mup), which can the be used to create additional Scanner Devices that target Modbus Servers of the same type.

AutomationDirect.com would prefer to have Modbus Profile for known Modbus devices; however, this is impractical for third-party devices that we cannot access or test. To facilitate the expansion of the device library, we will be allowing user to submit their device profile to be incorporated into Do-more Designer.

Here is the process for submitting your Device Profiles, or changes to existing Profiles:
1.	Clone the repository.
2.	Browse to the Customer Profiles directory and create folder with your company name.
3.	Make changes to your company directory (add new profiles or modify existing profiles).
4.	‘Commit’ changes and create a ‘Pull Request’ (this will trigger an email to AutomationDirect.com to look over the request).
5.	AutomationDirect will review the ‘Pull Request’ and ‘Merge’ it into the repository if it is approved.
