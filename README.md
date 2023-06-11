# Hyper-v-wondow11-home
enable hyper v in window 11


Windows 11 Home edition does not include support for Hyper-V. Hyper-V is a virtualization technology provided by Microsoft, primarily available in Windows 11 Pro, Enterprise, and Education editions.

process 1 -

pushd "%~dp0"
dir /b %SystemRoot%\servicing\Packages\*Hyper-V*.mum >hyper-v.txt
for /f %%i in ('findstr /i . hyper-v.txt 2^>nul') do dism /online /norestart /add-package:"%SystemRoot%\servicing\Packages\%%i"
del hyper-v.txt
Dism /online /enable-feature /featurename:Microsoft-Hyper-V -All /LimitAccess /ALL
pause


step 1 - copy abode code and paste in note pad and save as a hyperv.bat file .
step 2 - right click that hyperv.bat file and chose option run as administrator.
step 3- wait for complete .
step 4 - after complete restart pc.
step 5 - open control panel and go to progrmars optoin and click window feature turn on off.


process 2 -

step 1 - dowload .bat file in this github repo.
step 2 - right click that hyperv.bat file and chose option run as administrator.
step 3- wait for complete .
step 4 - after complete restart pc.
step 5 - open control panel and go to progrmars optoin and click window feature turn on off.


