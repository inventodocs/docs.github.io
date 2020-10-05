Visualziation, Mapping and Localization
----------------------------------------

Great Job! On reaching to this step. In this quick tutorial, we will guide you through mapping your environment with the robot. Before you continue with the below steps, please make sure you and your Robot are connected to the same WiFi Network. Take note of the IP Address of your system as well as the Robot (whose name will be rospc). If you are unable to get the IP address of your system and the robot with the help of your system administrator. The onther way around is as follows (not recommend):

1. Open the Terminal on your laptop. 

2. Run ifconfig (if not installed, you can install it by running **apt-get install net-tools**)

3. You would get three paragrahs on the terminal. Search for the paragraph titled **wlan0**. In that paragraph make note of inet address.

4. Incase you are not able to find the IP address of your Robot. Unscrew the back panel of the robot connect the NUC (A black color box) to a monitor using a hdmi cabel and run steps 1,2,3 again and make note of the IP adress. 

Running Mapping and Visualization
=================================

1. Turn your robot on and give it some time. You should see the LiDAR spinning after a few seconds. 

2. Once the LiDAR is spinning and you have confirmed it visually. Now its time to start the mapping. 

3. To visualize how you are mapping and making sure every corner is mapped. Download the script from the following **Link** and edit it to make sure it looks like this. (Replace YOUR_IP_ADDRESS with your IP address (laptop) and the ROBOT_IP_ADDRESS (with the IP address of NUC)

.. code-block:: python

   export ROS_IP= YOUR_IP_ADDRESS
   export NUC_IP= ROBOT_IP_ADDRESS
   export ROS_MASTER_URI="http://"$NUC_IP":11311"

4. Run the script by running ./script_name.sh (Replace the script_name with the name you have given while saving the script)

5. Post this step you should see a visuzlization tool and in a few seconds also load up a defauly map with two arrows represnting the robot on your screen.

6. To start mapping, open the roboremo application shared to you. Click the clear map button on the screen. In a few seconds you should see the default map being erased and an empty map starting to build.

7. Using the roboremo, keep moving the robot slowly around the environment and watch the map being built on the visulization tool. 

8. Feel Free to clear the map, incase you feel you are not satisfied and start again.

9. Once you are satisfied with the map of your arena. Click save map on your roboremo. This should save the map titled **NEW_MAP** inside the NUC automatically.

10. Restart your Robot and to verify if your robot has learnt the new map, repet steps 1 to 5 and you should now see the robot placed in your newly mapped environment. 

11. Phew! Great job on reaching here! You are just two steps away from making your robot Move Autonomously to your desired locations. 


Localization and Navigation
===========================
0. Please note all these steps will be performed on the Visualization tool.

1. In the visualization tool on the top you should see two clickable buttons named a. 2D pose Estimate and b. 2D Nav Goal.

2. These buttons are used for localization and Navigation respectively.

3. Have a look where the robot is located in your environment and which direction is it facing. Once you have noted where your robot is and facing, click on the 2D pose estimate button and place your cursor on the approximate position of the robot in the map and align the direction towrards the robots facing. 

4. This should move the arrows visible on the map to an approximate position within the map which is close to the actual location of the robot on the map.

5. Get ready for the fun part! Now choose a destination where you want your robot to navigate. Once you have made up your mind, Click on the 2D Nav goal button on your visualization tool and use the cursor to click on your desired destination. If everything goes well, you should see your robot mving to the desired location.

6. If you ever feel the robot is moving wierd or you notice the red lines (laser points) or not aligned to the black lines (obstacles) on the visualization tool, repet step 4 again (though this happes rarley, if the robot is not pushed around).

