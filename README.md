## exercise-1-modularity-leeb24
exercise-1-modularity-leeb24 created by GitHub Classroom


## Architecture Diagram & Explanation 

![Alt text](/Adiagram.png?raw=true "Diagram")

The whole architecture is operated on by using threads in python. Our architecture is mainly divided into 3 parts 
sensors, real-time processor and display. When the program starts the sensor module starts reading in the real values from the text file (virtual data) and passes it into the central queue. The central queue collects all the sensors readings and checks for any irregular activities. If a certain vital value is not within the normal range the real-time processor invokes a notification method that sends SMS,EMAIL or Telegram message to seek for help. The display module shows vital readings in a bar graph and also notifies the user if any irregular activity was to occur.
The whole system is semi asynchronous because we are using muti-threading and taking & processing the readings on the fly as they come in random time.

## Pros and Cons 

Pro - I think this architecture is very easy to scale functionality wise. Since we are collecting the data in the central queue, if we were to add a new Vital reading, we can simply plug in the module and pass the reading to the central queue.
The upper-level of the code is really abstract and modular so it is pretty easy for a new developer to follow the code.

Cons- There was an error in the display where the threads would interfere with each other before one could finish its process. We solved it by locking the threads untill it finished its process. 


## What would you improve on your code

Since most of the framework was already done. I would like to rebuild the framework in other completely asynchoronous language such as Node.JS
