#PowerShell

Install PowerShell plugin 1st.
Step by Step example: https://adamtheautomator.com/jenkins-powershell/
```PowerShell
# Create Temp Directory
if (-not(Test-Path -Path 'C:\temp'))
{
    New-Item -Path 'C:\temp' -ItemType directory
}

# Using the environment variables exposed by the Jenkins job 
Set-Content -Path "C:\temp\$($env:Filename).txt" -Value $env:Message
```
