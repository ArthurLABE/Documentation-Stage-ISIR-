# Documentation Stage ISIR on LeKiwi Robot
Description of our progression to train the robot LeKiwi. The goal is to make it take a box and place it in another location all by itself after the fine-tuning based on our own dataset.
We used https://wiki.seeedstudio.com/lerobot_lekiwi/ to help us, our page is just a complementary description of this one.

# I- LeRobot Teleoperation 
In this part, we describe how we managed to teleoperate the follower arm by moving the leader arm.

1st step : Setup the motors if it's not already done

Find USB ports associated to your arms To find the correct ports for each arm, run :
```
lerobot-find-port
```

<img width="4096" height="2304" alt="image" src="https://github.com/user-attachments/assets/c74c6403-2869-41aa-b369-54ce571fef8a" />



