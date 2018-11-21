#-----------------------------------------------------------------------------------------------------------------------------------------------------------------#
#baseproject-template-selenium-browser v1
#Date - 07/27/2018
#Confluence URL - https://cedt-confluence.nam.nsroot.net/confluence/pages/viewpage.action?pageId=457983685
#-----------------------------------------------------------------------------------------------------------------------------------------------------------------#

What is new:
New BDD program for CBOL Sign On, with;
	- Testng Framework
	- Page Factory model
	- Chrome as Windows OS Webdriver
	- Phantomjs headless as Linus OS webdriver
	- Executables controlled through POM.XML
	- Jenkins Setup

#-----------------------------------------------------------------------------------------------------------------------------------------------------------------#
#baseproject-template-selenium-browser v2
#Date - 10/08/2018
#Confluence URL - https://gct-cedt-pilot.nam.nsroot.net:8090/confluence/download/attachments/10521808/cbolsignonv2.zip?api=v2
#-----------------------------------------------------------------------------------------------------------------------------------------------------------------#

What is new:
Enhancements on existing BDD program

	- Shapelayer implementation for Chrome and Phantom webdrivers
	  https://cedt-confluence.nam.nsroot.net/confluence/display/160358/23+Bypass+Shape+layer+while+running+Selenium+script
	  
	- Selenium driver with driver retry (avoid driver initialization issue on VDIs)
	- Selenium driver quit/null options to free up memory space
	- Selenium driver killing all existing taks before initializing driver
	
	- Test Data Overriding to Feature file
		- Added a method on runner class to override feature files with data from specified excel

	- Requirement Traceability - added naming convention for scenario outline, which helps to generate Requirement Traceability matrix sheet
		- Scenario Outline: <Scenario Summary> : <US# - US Summary>; <US# - US Summary>
		- CreateExlFile and writeExlFile methods on ExcelUtils class will be used to generate Requirement Traceability matrix sheet
		
	- Common Functions class added for regular actions such as Click, SendKeys, Element Visibility etc
	
	- Nexus to Artifactory update
	  https://cedt-confluence.nam.nsroot.net/confluence/display/160358/22+Nexus+to+Artifactory

	- Jenkins Email Notification with results on Body of the email (controlled through POM.xml)
		
	- POM Updated to reflect all above changes / dependencies
	
	------------------- 10/11/2018-----------------10 AM CST
	
	- Added logic to enable LocalProxyStart and Stop services only for windows OS
	- Excel Reader enhanced to fetch data depends on the scenario to be executed.
	
	------------------- 10/11/2018-----------------4 PM CST
	
	- Selenium Driver class updated to handle driver unavailable. 
		- Try part - will setup driver, if its already exist
		- Catch part - will download if there is no active driver
	