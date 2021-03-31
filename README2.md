For those of you that are having issues with the shop not taking money and some other boolean errors. Or even getting the server running then follow these steps.

1. DO NOT DOWNLOAD THE ZIP FROM GITHUB! You MUST CLONE the Git instead using Github for desktop.
2. Download the latest FiveM build from here - https://runtime.fivem.net/artifacts/fivem/build_server_windows/master/
3. Extract the FiveM build files to a location on your drive eg c:\nopixel
4. Go to the Cloned Git folder of the nopixel server on your desktop and COPY the entire contents to the same folder you created in step 3. (not the main folder but the contents of the main folder where you see the FXServer.exe etc. Yes to overwrite files.
5. Edit start.bat to point to correct path of run.cmd eg start c:\nopixel\run.cmd
6. Edit run.cmd ro point to FXServer within the nopixel folder that we created eg powershell "D:\nopixel\FXServer.exe +exec resources.cfg +exec server.cfg +set onesync on +set sv_enforceGameBuild 2189| tee console_$(Get-Date -f yyyy-MM-dd-HHmm).log
7. Using XAMP and HeidiSQL and the nopixel.sql script create your DB.
9. Edit the server.cfg as you would with any other server steamdID and sv_licenseKey. Make sure that the server.cfg allows only 48 connections.
10. Clear your FiveM cache and server cache if you have run it before now. Clear your FiveM cache regardless.
10. Start server by running start.bat