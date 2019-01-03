## General 
Question1 :Explain a recent project you've worked on. Why did you choose this project? 
What difficulties did you run into this project that you did not expect, and how did you solve them?

Answer: I have workded on game to system project expension working with Aristocrate for NSW extesion/adaption.
This project is choose as the latest project with my current employer for the same.

Strict timeline, first developement in sydney centre ,No document, Large code base need to update/extend adapt as specification.

Add document from code base by doxygen, resloving issue day by day with help of simulator for diffrent event, message by adding c++ code for the protocol.

## Mandatory 
Question 2 :What are some of the advantages & disadvantages of cameras, lidar and radar? What combination of these (and other sensors) would you use to ensure appropriate and accurate perception of the environment?
Answers : Cameras, lidar and radar are the eyes of self driving car , 
Camaera : A camera is fundamentally a sensor that grabs a bunch of color points in space and arranges them into an image, often referred to as an image array. This image array is converted into a digital signal and is passed along to the hardware that does sensor fusion and scene understanding.
Lidar : LiDAR is a laser-light point-and-shoot methodology for sensing the world. A transmitter spits out a bit of light, waits for that light to bounce off an object, and since it knows how fast light travels, can determine how far away that object is by determining the time that’s passed between sending out that light and receiving it. LiDAR units can broaden their field of view by using a bunch of lasers that spin around in a circle, or more recently, as a stationary bunch of lasers that spread out along a field of view, called “Solid State LiDAR.” After all the light is received, the LiDAR system sends an array of direction and distance information back to the hardware for sensor fusion and scene understanding, referred to as a “point cloud.
Radar : Radar has been around forever. It is similar to LiDAR in that it is a “point-and-shoot” technology, but uses radio, or electromagnetic, waves to do this. Radar lends itself well to long-distance object detection but is not typically very precise.
So how do you test this thing? Well, it’s just like LiDAR, but since the RADAR technology is less expensive and better understood, some companies are already creating tools for this purpose:

please see the image below to ensure appropriate and accurate perception of the environment.

add figure here

Figure 1: McKinsey&Company Evaluation of Autonomous Vehicle Sensors
---------------------------------------------------------------------------------------------------------------------------
Question 3 :Describe the overall process of how a basic Kalman Filter works. Where might a basic Kalman Filter be less than sufficient? How can you improve the basic algorithm to improve performance in such a situation?

Answers :Kalman Filters, also known as linear quadratic estimation (LQE), is an algorithm that helps us to obtain more reliable estimates from sequence of observed measurements(sensor measurements).

It can be used to track the position and velocity of a moving pedestrian over time and also measure the uncertainty associated with them. It is basically a two-step iterative process.
Predict 🤔
Update ✍️

Actually, Kalman Gain is a parameter which decides how much weight should be given to predicted value and the measured value. It checks the uncertainty in both predicted value and measured value and then it decides whether our actual value is close to predicted value or measured value.
K = Error In Prediction / (Error in Prediction + Error in Measurement)
Error In Measurement is generally given by the sensor manufacturers. When we buy a new sensor, the manufacturer tells us the standard deviation of the measurement that we’ll get from the sensor. It means, let say the standard deviation is 3 and actual measurement is 150, then the sensor can give us the output ranges from 147–153.
Error In Prediction is calculated mathematically. We initially start with a wrong belief(large error) and then reduces the error gradually(using Kalman Gain) after taking the first few measurements from the sensor.

put the image here link<https://www.youtube.com/watch?v=Fuy73n6_bBc>

Basic kalman filter is less than sufficent if we have non liner measurement function.

we have to use extended kalman filter by using first order of taylor expansion to construct a linear approximation.

Question 4 :How does an Extended Kalman Filter differ from a regular Kalman Filter? Provide an example of where an EKF would be necessary or an improvement, and detail why it would be needed in that situation.

Question 5 :What is the difference between an Extended Kalman Filter and an Unscented Kalman Filter? In what situations would there be larger differences between the two approaches?

## Coding
Question 6 :[Code] Explain the steps behind how an Extended Kalman Filter is implemented.
Answer : Added the extended kalman filetr impelementation and the commnet are self explaratory.





