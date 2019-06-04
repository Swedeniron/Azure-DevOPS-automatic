# Azure-DevOPS-automatic
Create projects in Azure DevOps with users, group and repos


This set of PowerShell scripts will allow you to manage and create a VSTS project. The following files are included.

CreateProject.ps1 - This file will control the adding of a project
                                           adding teams to the project
                                           adding VSTS groups
                                           adding a Git Repo
                                           adding security to groups within the project
                                           
ProjectDej.json - This json file will hold the parameters needed to create a project, add teams, users and security
                  It also includes the PAT or Personal access token needed to connect to the VSTS instance.
                  
ProjectAndGroup.psm1 - this Module contains the functions needed for the project

Helper.psm1 - this module contains helper functions

SecurityHelper.psm1 - this module contains security related functions

It will complain on wrong permissons:
Open a powershell in admin mode
Go to the dir where the script are

Get-ExecutionPolicy -List

        Scope ExecutionPolicy
        ----- ---------------
MachinePolicy       Undefined
   UserPolicy       Undefined
      Process       Undefined
  CurrentUser       Undefined
 LocalMachine    RemoteSigned

Change the RemoteSigned Policy:

Set-ExecutionPolicy -ExecutionPolicy Undefined -Scope LocalMachine

Execution Policy Change
The execution policy helps protect you from scripts that you do not trust. Changing the execution policy might expose you to the security risks described in the about_Execution_Policies help topic at
https:/go.microsoft.com/fwlink/?LinkID=135170. Do you want to change the execution policy?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y


List the Policy again:

Get-ExecutionPolicy -List

        Scope ExecutionPolicy
        ----- ---------------
MachinePolicy       Undefined
   UserPolicy       Undefined
      Process       Undefined
  CurrentUser       Undefined
 LocalMachine    Unrestricted
