## Muldrop
This Trojan arrives on a system as a file dropped by other malware or as a file downloaded unknowingly by users when visiting malicious sites.

Installation

This Trojan adds the following processes:

    %System%\Robocopy.exe robocopy Install\Install_UI\m_driv %Windows%\Resource /mir
    sc create "Windows Resource Kit" start= auto error= ignore binpath= "%Windows%\srvany.exe"
    reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Windows Resource Kit\Parameters" /v Application /t REG_SZ /d "%Windows%\Resource\run.exe" /f
    reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Windows Resource Kit\Parameters" /v AppDirectory /t REG_SZ /d "%Windows%\Resource" /f
    setx path "%All Users Profile%\Oracle\Java\javapath;%System%;%Windows%;%System%\Wbem;%System%\WindowsPowerShell\v1.0\;%System Root%\Python27;%System Root%\Python27\Scripts;%Windows%\Resource"
    Install\r.exe 

(Note: %Windows% is the Windows folder, where it usually is C:\Windows on all Windows operating system versions.. %System Root% is the Windows root folder, where it usually is C:\ on all Windows operating system versions.)

It creates the following folders:

    %Windows%\Resource

(Note: %Windows% is the Windows folder, where it usually is C:\Windows on all Windows operating system versions.)

Autostart Technique

This Trojan registers itself as a system service to ensure its automatic execution at every system startup by adding the following registry entries:

    HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\
    Services\Windows Resource Kit
    ImagePath = "%Windows%\srvany.exe"

Other System Modifications

This Trojan adds the following registry entries:

    HKEY_CURRENT_USER\Software\Microsoft\
    ResKit\Robocopy
    WaitTime = "30000"

    HKEY_CURRENT_USER\Software\Microsoft\
    ResKit\Robocopy
    RetryMax = "1000000"

    HKEY_CURRENT_USER\Software\Microsoft\
    ResKit\Robocopy
    JobDir = "::"

    HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\
    services\Windows Resource Kit\Parameters
    Application = "%Windows%\Resource\run.exe"

    HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\
    services\Windows Resource Kit\Parameters
    AppDirectory = "%Windows%\Resource"

    HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\
    Services\Windows Resource Kit
    DisplayName = ""

    HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\
    Services\Windows Resource Kit
    Start = "SERVICE_AUTO_START"

It modifies the following registry entries:

    HKEY_CURRENT_USER\Environment
    path = "{random characters}"

(Note: The default value data of the said registry entry is %Program Files%\Microsoft Visual Studio\Common\Tools\WinNT;%Program Files%\Microsoft Visual Studio\Common\MSDev98\Bin;%Program Files%\Microsoft Visual Studio\Common\Tools;%Program Files%\Microsoft Visual Studio\VC98\bin.)

This report is generated via an automated analysis system.
