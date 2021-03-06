﻿Publishes a Windows Azure Web App from a Web Deploy Package using MSDeploy
==========================================================================

            

<#





.SYNOPSIS


Publishes a Windows Azure Web App from a Web Deploy Package.


Adapted from Scott Guthrie's Publish-AzureWebsite.ps1 script included


with the FixIt application at:


https://code.msdn.microsoft.com/Fix-It-app-for-Building-cdd80df4


 


.DESCRIPTION


To run this script, you must have a Windows Azure


Web App (formerly website) associated with your Windows Azure account.


To verify, run the Get-AzureWebsite cmdlet.


You must also have Wed Deploy (MSDeploy.exe) installed at:


C:\Program Files\IIS\Microsoft Web Deploy V3\


If installed elsewhere, modify the $msbuildPath variable.


 


.PARAMETER WebDeployFile


Specifies the ZIP file generated by the Web Deploy Package.


This parameter is required.


Recommend having this file local to the script in order to avoid passing a path;


this is due to quirks getting MSDeploy to run from PS.


.PARAMETER SetParametersFile


Specifies the SetParameters file generated by the Web Deploy Package.


This parameter is required.


Recommend having this file local to the script in order to avoid passing a path;


this is due to quirks getting MSDeploy to run from PS.


.PARAMETER PublishSettingsFile


Specifies the Publish Settings file.


This parameter is required.


.INPUTS


System.String


.OUTPUTS


None. This script does not return any objects.


.NOTES


This script automatically sets the $VerbosePreference to Continue,


so all verbose messages are displayed, and the $ErrorActionPreference


to Stop so that non-terminating errors stop the script.


MSDeploy can be tricky to run from PS. I recommend running this script from the same location


as the 3 files that are passed as parameters.


.EXAMPLE


Publish-AzureWebApp.ps1 -WebDeployFile ContosoAdsWeb.zip -SetParametersFile ContosoAdsWeb.SetParameters.xml -PublishSettingsFile Contoso-app01.PublishSettings


 


#>





 
 







 



 



 


 

** *** *




 


        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
