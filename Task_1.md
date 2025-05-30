  

### Task 1

---

You have been placed in charge of designing a **robust monitoring system** for the rovers computation system (Raspberry Pi, Jetson Nano, STM's, etc). You have to monitor the **CPU usage** and the **temperate** of your device (Your laptop for now) and if it exceeds above a certain limit you need to shutdown the rover.

  

1. Make a Node which will obtain the current CPU usage as well as the temperature and publish this information on separate topics /CPU and /temp.

2. Make another node which will subscribe from this data and based on the below conditions will perform the necessary action


| CPU Usage  | Process |
| ------------- | ------------- |
| 0.5 - 0.99  | Output "LOW CPU USAGE" using ROS Warning loggers |
| 1.0 - 1.99  | Output "Normal CPU USAGE" using ROS Info loggers |
| > 2.0 | Output "Critical CPU USAGE" using ROS fatal loggers and shutdown ROS |

| Temperature  | Process |
| ------------- | ------------- |
| < 19°  | Output "Low Temperature" using ROS Warning loggers |
| 20° - 59°  | Output "Normal Temperature" using ROS Info loggers |
| > 60° | Output "Time to buy a new Pi" using ROS fatal loggers and shutdown ROS |

Also create another node called utility which counts all the publishers, subscribers for both the topics and also counts the total number of active nodes.

#### Reference

1. https://github.com/ros2/rclpy/blob/humble/rclpy/rclpy/node.py
2. https://stackoverflow.com/questions/276052/how-to-get-current-cpu-and-ram-usage-in-python
3. https://stackoverflow.com/questions/2440511/getting-cpu-temperature-using-python#comment99168080_2440539
4. https://github.com/ros2/rclpy/blob/a7c8631c7af567b01adc15406bd02825b5276642/rclpy/rclpy/impl/rcutils_logger.py

> [!TIP]
> Click this on the Github page to view all the methods of a class
> <img width="515" alt="Screenshot 2025-05-30 at 7 19 26 PM" src="https://github.com/user-attachments/assets/cef1a0bb-0d96-462c-a46a-58a13dd9ac19" />



### Task 2
---
Create a Node to obtain camera data (the camera should be recording an object of distinct color) using OpenCV and publish it to a topic called image_raw. Another Node should subscribe from that topic and move the turtlesim robot in such a way that it follows the direction of the distinctly colored object.

**Example**: 

https://github.com/user-attachments/assets/e89a5430-8ecb-4c6c-b942-45c1caa5dee3

### Deadline
---
On or before Monday.\
If you have any questions or trouble figuring stuff out message me on whatsapp

 -Naren
