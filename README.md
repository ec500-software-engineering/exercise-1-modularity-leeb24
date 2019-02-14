# exercise-1-modularity-leeb24
exercise-1-modularity-leeb24 created by GitHub Classroom


# Architecture Diagram & Explanation 

![Alt text](/Adiagram.png?raw=true "Diagram")

The whole architecture is operated on by using threads in python. Our architecture is mainly divided into 3 parts 
sensors, real-time processor and display. When the program starts the sensor module starts reading in the real values from the text file (virtual data) and passes it into the central queue. The central queue collects all the sensors readings and checks for any irregular activities. If a certain vital value is not within the normal range the real-time processor invokes a notification method that sends SMS,EMAIL or Telegram message to seek for help. The display module vital readings 

# Pros and Cons 




# What would you improve on your code
