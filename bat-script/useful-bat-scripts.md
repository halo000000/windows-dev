---
icon: bat
---

# useful bat scripts

#### **1. Backup a Folder**

Asks the user for source and destination paths for the backup.

```bat
@echo off
set /p source="Enter the source folder path: "
set /p destination="Enter the destination folder path: "
xcopy "%source%" "%destination%" /E /H /C /I
echo Backup completed from "%source%" to "%destination%".
pause
```

***

#### **2. Delete Temporary Files**

Confirms with the user before deleting temp files.

```bat
@echo off
echo This will delete all temporary files. Do you want to continue? (Y/N)
set /p choice=
if /i "%choice%"=="Y" (
    del /s /q %temp%\*
    rd /s /q %temp%
    echo Temporary files deleted.
) else (
    echo Operation canceled.
)
pause
```

***

#### **3. Ping a Server**

Lets the user input a website to ping.

```bat
@echo off
set /p server="Enter the website or IP to ping: "
ping %server% -n 5
pause
```

***

#### **4. Automate Disk Cleanup**

Displays a message before running disk cleanup.

```bat
@echo off
echo This will run the Disk Cleanup tool. Press any key to continue.
pause
cleanmgr /sagerun:1
echo Disk cleanup completed.
pause
```

***

#### **5. Shutdown Timer**

Allows the user to input the delay (in seconds) before shutdown.

```bat
@echo off
set /p delay="Enter the shutdown timer (in seconds): "
shutdown -s -t %delay%
echo The system will shut down in %delay% seconds.
pause
```

***

#### **6. Restart Network Adapter**

Asks the user to confirm before restarting the network adapter.

```bat
@echo off
echo This will restart your Wi-Fi adapter. Do you want to proceed? (Y/N)
set /p choice=
if /i "%choice%"=="Y" (
    netsh interface set interface "Wi-Fi" admin=disable
    timeout /t 5
    netsh interface set interface "Wi-Fi" admin=enable
    echo Wi-Fi adapter restarted.
) else (
    echo Operation canceled.
)
pause
```

***

#### **7. Automate Software Installation**

Prompts the user to enter the application file path for installation.

```bat
@echo off
set /p filepath="Enter the path of the installer (e.g., C:\Setup.exe): "
start /wait "%filepath%" /S
echo Installation completed for "%filepath%".
pause
```

***

#### **8. Clear DNS Cache**

Confirms with the user before clearing DNS cache.

```bat
@echo off
echo Do you want to clear the DNS cache? (Y/N)
set /p choice=
if /i "%choice%"=="Y" (
    ipconfig /flushdns
    echo DNS cache cleared.
) else (
    echo Operation canceled.
)
pause
```

***

#### **9. Monitor Disk Space**

Displays available disk space.

```bat
@echo off
echo Displaying disk space information...
wmic logicaldisk get size,freespace,caption
pause
```

***

#### **10. Automated File Renaming**

Asks for the file extension and renames files.

```bat
@echo off
set /p extension="Enter the file extension to rename (e.g., .txt): "
for %%f in (*%extension%) do ren "%%f" "Renamed_%%f"
echo All %extension% files renamed.
pause
```

***

#### **11. Extract ZIP Files**

Prompts the user for the ZIP file path and extraction destination.

```bat
@echo off
set /p zipfile="Enter the path to the ZIP file: "
set /p destination="Enter the destination folder: "
powershell -command "Expand-Archive -Path '%zipfile%' -DestinationPath '%destination%'"
echo ZIP file extracted to %destination%.
pause
```

***

#### **12. Create a Wi-Fi Hotspot**

Asks for SSID and password.

```bat
@echo off
set /p ssid="Enter the Wi-Fi hotspot name (SSID): "
set /p key="Enter the Wi-Fi hotspot password: "
netsh wlan set hostednetwork mode=allow ssid=%ssid% key=%key%
netsh wlan start hostednetwork
echo Hotspot '%ssid%' created and started.
pause
```

***

#### **13. Schedule a Task**

Prompts the user for task details.

```bat
@echo off
set /p taskname="Enter the name of the task: "
set /p filepath="Enter the path to the batch file/script to run: "
set /p time="Enter the time to run the task (HH:MM): "
schtasks /create /tn "%taskname%" /tr "%filepath%" /sc daily /st %time%
echo Task '%taskname%' scheduled at %time%.
pause
```

***

#### **14. Check System Uptime**

Displays system uptime.

```bat
@echo off
echo Checking system uptime...
systeminfo | find "System Boot Time"
pause
```

***

#### **15. Block a Website**

Asks for a website to block.

```bat
@echo off
set /p website="Enter the website to block: "
echo 127.0.0.1 %website% >> %windir%\System32\drivers\etc\hosts
echo Website '%website%' blocked.
pause
```

***

#### **16. Copy Files Based on Extension**

Asks for file extension and destination.

```bat
@echo off
set /p extension="Enter the file extension to copy (e.g., .jpg): "
set /p destination="Enter the destination folder: "
xcopy *%extension% "%destination%" /s /i
echo All %extension% files copied to %destination%.
pause
```

***

#### **17. Check Open Ports**

Lists open ports.

```bat
@echo off
echo Checking open ports...
netstat -an | find "LISTENING"
pause
```

***

#### **18. Enable Hibernate Mode**

Confirms with the user before enabling hibernation.

```bat
@echo off
echo This will enable hibernate mode. Do you want to proceed? (Y/N)
set /p choice=
if /i "%choice%"=="Y" (
    powercfg /hibernate on
    echo Hibernate mode enabled.
) else (
    echo Operation canceled.
)
pause
```

***

#### **19. Create a System Restore Point**

Asks for a description for the restore point.

```bat
@echo off
set /p description="Enter a description for the restore point: "
powershell -command "Checkpoint-Computer -Description '%description%' -RestorePointType 'MODIFY_SETTINGS'"
echo Restore point '%description%' created.
pause
```

***

#### **20. Auto-Connect to a VPN**

Prompts the user for VPN credentials.

```bat
@echo off
set /p vpnname="Enter the VPN connection name: "
set /p username="Enter the VPN username: "
set /p password="Enter the VPN password: "
rasdial "%vpnname%" %username% %password%
echo Connected to VPN '%vpnname%'.
pause
```

***

#### 21.Create Event Log

```
@ECHO OFF
IF "%~1"==" /?" GOTO HELP

TIMEOUT /T 10
:BEGIN
EVENTCREATE /T ERROR /L APPLICATION /ID 100 /D "This is your error message."
GOTO END

:HELP
ECHO This batch file waits for 10 seconds and then logs an error event in the Application log.
ECHO Usage:
ECHO    MyBatchFile.bat         Run the batch file normally.
ECHO    MyBatchFile.bat /?      Display this help message.
GOTO END

:END
```

***

#### 22. send Email

```
powershell -ExecutionPolicy ByPass -Command Send-MailMessage ^
    -SmtpServer smtp.your_domain.com ^
    -To to_email@your_domain.com ^
    -From from_email@your_domain.com ^
    -Subject Email Subject Test ^
    -Body Email Body Test
```

***

#### 23. ftp file stransform&#x20;



```
open FTP sftp.your_ftp_server.com
Username
Password
prompt
bin
rename File_Name*.csv C:\\File_Path\File_Name*.csv
del File_Name*.csv
bye
```

***

#### 24. kill a program

```
:: Kill Task
taskkill /f /im Program_To_Kill.exe

:: Prompt Box
echo msgbox "Program has been successfully killed!" > %tmp%\tmp.vbs
cscript /nologo %tmp%\tmp.vbs
del %tmp%\tmp.vbs
```







