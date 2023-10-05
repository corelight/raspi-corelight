# Corelight@Home (`raspi-corelight` v3.2)

### Configure the Pi to Run Corelight Software Sensor 

The Corelight Software Sensor is a 64-bit application, so we have created a configuration tool `raspi-corelight` to perform initial configuration of the sensor and Raspberry Pi OS.  To install and run this tool, perform the following from a terminal window on your Raspberry Pi:

**For official Raspberry Pi OS (64bit)**

Install `raspi-corelight` from Github by executing the following (all on one line):

     source <( curl https://raw.githubusercontent.com/corelight/raspi-corelight/main/raspi-corelight)

The script will then download the Software Sensor package from the repository and install it.  

Press Enter to start the configuration tool. There will be errors in the Status section of the main menu since you have not installed a license and the service is not yet started. 
 
Select option 6 (Quick Config) to configure monitor port, enter your license information, and set up Falcon LogScale or Splunk export.  
Note that to define the monitor port, you must enter a value (such as `eth0`) at the prompt, and you will be prompted to accept any changes entered. 

You can execute the script at any time with the following command:

     raspi-corelight

This completes the installation of the Corelight Software Sensor for Corelight@Home.  You should have network metadata and alerts flowing into your configured data repository. For any installation questions, comments or technical support issues, please read (and contribute to) the `#Corelight_at_Home` channel on Corelight's Community Slack workspace (https://corelightcommunity.slack.com). For issues downloading a license or accessing the Slack space, email CorelightAtHome@corelight.com.


