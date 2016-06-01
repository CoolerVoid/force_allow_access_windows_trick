# force_allow_access_windows_trick

#### Force allow access in windows firewall

What if I tell you that you can use Windows API to simulate a keystroke so as to bypass firewall checks?

 Windows has the function SendInput() to simulate a keystroke. This function accepts as argument an array of INPUT structures. The INPUT structures can be either a mouse or a keyboard event. The keyboard event structure has a member called wVk which can be any key on the keyboard.

SendInput() played an important role when writing the code for bypassing Windows firewall. How does it work? 

Firstly, it finds a window with title 'Windows Security Alert' using the function GetWindowText(). Secondly, it calls SendInput() with TAB and ENTER keys to choose button 'allow access'. As simple as that


