# Documentation Stage ISIR on LeKiwi Robot
Description of our progression to train the robot LeKiwi. The goal is to make it take a box and place it in another location all by itself after the fine-tuning based on our own dataset.
We used https://wiki.seeedstudio.com/lerobot_lekiwi/ to help us, our page is just a complementary description of this one.
          <img width="667" height="517" alt="image" src="https://github.com/user-attachments/assets/6728a1d9-207e-48da-9134-d22c5fac0231" />


# I- LeRobot Teleoperation 
In this part, we describe how we managed to teleoperate the follower arm by moving the leader arm.
We followed the following wiki that describe the method step by step : https://wiki.seeedstudio.com/lerobot_so100m/
In term of steps : setup motors, calibrate them, teleoperate.

# II- Key points when recording the dataset
By following the same wiki, we manage to record a dataset of 20 episodes. 
By fine-tuning our model on this dataset, we identified some problems that have affected operation : 

  - The delay caused by the cameras : Our VLA model use real time video to instruct the robot to perform a chunk of actions, if the delay from cameras is to significant, the robot perform the actions to late and then has to correct itself which causes also a delay and prevents it from completing the task.
    
  - Lack of diversity : With only 20 episodes, we were unable to observe a sufficient variety of actions, such as the robot reversing after getting too close to the box to grab it. It is essential to incorporate maximum diversity into the dataset, particularly in terms of starting positions, box positions, and the external environment, to make the model as versatile as possible.



