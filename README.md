# Credential_Exposure_Assessment
Script to run to assess potentially exposed credentials on Windows in the case of a malware event or suspected credential theft attack on a system

Script will pull information related to:

 1. Terminal Services Logins
 2. Scheduled Task Stored Credentials
 3. Services Running with Stored Credentials
 4. Currently Running Processes running under user accounts
 5. All User Logon Events by Logon Event Type (2,4,5,8,9,10, * 11 LogonTypes)
 6. Cached Credentials (CMDKEY /LIST Output)
 7. Credentials stored in Browsers (Chrome, Edge, Firefox, Brave, Vivaldi, Opera, OperaGX)

#Requirements
Must be run as local administrator

#Artifacts
This script does SOME writing to the local disk - things to be aware of:

 1. May create a folder c:\Temp if it does not already exist
 2. Writes temporary .SQL files with random names into the C:\Temp directory (should also delete them)
 3. Writes output of script to a Full Path Directory of your choosing
