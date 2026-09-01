# Instructions For Klipper
1. First, go into ur Klipper page and go to the Machine tab.
<img width="959" height="437" alt="image" src="https://github.com/user-attachments/assets/db305834-a49c-4725-880f-7f685e500685" />
2. Once ur there, scroll and look for the file named "printer.cfg"   NOTE: It must be that exact file, not something like "printer-
20260810_190809.cfg"
<img width="375" height="290" alt="image" src="https://github.com/user-attachments/assets/4111e542-221d-40a1-adb9-b6e4d208aece" />
3. Once ur inside this folder, scroll all the way to the bottom and add this code block: 

[filament_switch_sensor runout_sensor]
pause_on_runout: True
switch_pin: ^PC15

4. Click Save & Restart
<img width="955" height="443" alt="image" src="https://github.com/user-attachments/assets/fd656185-c2b8-43e9-9588-c5c9a3522831" />

5. Test it.
