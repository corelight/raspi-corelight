# Configure the Pi to Run Corelight Software Sensor

The Corelight Software Sensor is a 64-bit application, so we have created a configuration tool raspi-corelight) to facilitate that kernel upgrade and perform initial configuration of the sensor.  To install and run this tool, perform the following from a terminal window on your Raspberry Pi:

Install raspi-corelight from Github by executing the following (all on one line):

     source <( curl https://raw.githubusercontent.com/corelight/raspi-corelight/main/raspi-corelight)

Execute the script with the following command:

     raspi-corelight

The script will begin the upgrade to the Raspian 64-bit kernel if necessary (most Raspian installs are 32-bit).  Follow the prompts, noting that the default response to the queries may be ‘No’, and you must actively answer ‘Y’ or the upgrade will halt.  Your Pi will reboot to finish the upgrade.

Log back in and run raspi-corelight again from the terminal.  If the upgrade above completed and Raspian is running the 64-bit kernel, the script will now prompt you to configure credentials for the authenticated installation repository for the Software Sensor, using your iDaptive user ID and password you set up during registration.

The script will then download the Software Sensor package from the repository and install.  

Press Enter to start the configuration tool. There will be errors in the Status section of the main menu since you have not installed a license and the service is not yet started. 
 
Select option 6 (Quick Config) to configure monitor port, enter your license information,  and set up Humio or Splunk export.  
Note that to define the monitor port, you must enter a value (such as eth0) at the prompt, and you will be prompted to accept any changes entered. 

This completes the installation of the Corelight Software Sensor for Corelight@Home.  You should have network metadata and alerts flowing into your configured data repository. For any installation questions, comments or support issues, please email CorelightatHome@corelight.com or read (and contribute to) on the #Corelight_at_Home channel on Corelight's Community Slack workspace (https://corelightcommunity.slack.com).


