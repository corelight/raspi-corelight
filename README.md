# Corelight@Home (raspi-corelight v3.1)

### Configure the Pi to Run Corelight Software Sensor 

The Corelight Software Sensor is a 64-bit application, so we have created a configuration tool `raspi-corelight` to perform initial configuration of the sensor and Raspberry Pi OS.  To install and run this tool, perform the following from a terminal window on your Raspberry Pi:

**For official Raspberry Pi OS (64bit)**



Install `raspi-corelight` from Github by executing the following (all on one line):

     source <( curl https://raw.githubusercontent.com/corelight/raspi-corelight/raspi64/raspi-corelight)

Execute the script with the following command:

     raspi-corelight


The script will now prompt you to configure credentials for the authenticated installation repository for the Software Sensor, using your iDaptive user ID and password you set up during registration.

The script will then download the Software Sensor package from the repository and install.  

Press Enter to start the configuration tool. There will be errors in the Status section of the main menu since you have not installed a license and the service is not yet started. 
 
Select option 6 (Quick Config) to configure monitor port, enter your license information,  and set up Humio or Splunk export.  
Note that to define the monitor port, you must enter a value (such as eth0) at the prompt, and you will be prompted to accept any changes entered. 

This completes the installation of the Corelight Software Sensor for Corelight@Home.  You should have network metadata and alerts flowing into your configured data repository. For any installation questions, comments or support issues, please email CorelightatHome@corelight.com or read (and contribute to) on the #Corelight_at_Home channel on Corelight's Community Slack workspace (https://corelightcommunity.slack.com).


