Steps to setup a new robot 
--------------------------

1. Check battery voltages using a multimeter
2. Check if there are three cables going out, two to the slamtec board including the lan cable. One goes to the motor driver board.
3. Using another PC, log in to the modem page [Password: admin] and check the list of wireless devices and find 'rospc'. Note down its IP address.
4. SSH into that IP address and use the password 'nav<///'.
5. Run the following and debug any errors.::

   'systemctl status nav_mitra.service' 
   'systemctl status freedomrobotics.service'

6. Get the command to install Freedom from the Freedom admin and run it in a terminal. A sample command - 'curl -sSf "https://api.freedomrobotics.ai/accounts/ALKJSFIJ32U4883957890485/devices/D4974622C1B99902DDB90F1B5A5/installscript?mc_token=T2bca965d0d0fd9ba2372c468&mc_secret=S9ae51396b71fe686be5f8d36&install_elements=webrtc&auto_install_deps=true&ppa_is_allowed=true" | python'

