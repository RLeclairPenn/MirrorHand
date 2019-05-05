# This is Mirror Hand!
### By: Rafael Gerkhe and Raul Leclair

Currently available prosthetics are either completely mechanical, with limited independent movement between joints, or costs thousands of dollars and require surgery to create an interface between nerves and the system. **Mirror Hand** proposes a way of improving low-cost prosthetics in cases where the user has an able hand, so that we can have it control the movements of the prosthetic. Therefore, adding functionality to the prosthetic by giving greater control over the prosthetic fingers to the user. 


## Week 1 

### April 10

We started constructing the glove which will have the flex sensors (SparkFun SEN-10264) that will give us the position of the able hand's fingers in order to translate them to a prosthetic. So far we have sewed the flex sensors into a glove.

[Insert April 10_1]

We connected the sensors to a multimeter to measure the resistance and check if it changed when we flexed which it did.

[Insert April10_2] and [Insert April0_3]

We learned that flex sensors are not entirely flexible when all five of the flex sensors we had broke. The reason they broke being that one of the "flexible" parts is not supposed to be flexed and if it is flexed there is a risk that the thin metallic sheet is broken as shown below. 

[Insert April10_5]

### April 11

With the flex sensors broken, we had to disarm the glove entirely. Luckily for us we had an extra flex sensor. We used the following equation to be able to calibrate the sensor on the range of 0-100 for better use. 

## Week 2

### April 18
The flex sensors arrived and we secured the place at which they could break with shrink wrap so that they stayed solid. We sewed and glued them to the hand and we got the readings we needed.

Over the weekend we printed the open-source prosthetic hand (https://www.thingiverse.com/thing:596966) which ended up being somewhat smaller than we predicted. 

[Insert April18_1]

Nonetheless, we assembled it and started tying the strings to the fingers. We used some flexible string we bought and yellow cord from Detkin.

[Insert April18_2]

Once one of the fingers was tied up we attached it to a servo and had it flex and unflex the finger.

[Insert April18_4]

Additionally, we set up the bluetooth modules (HC05) to communicate exclusively with each other. We connected them to two different mBeds and had them communicate. Once we were able to send messages in between the mBeds we started sending the data from the glove to the mBed that would control the prosthetic. We were succesful in doing so and were able to control the one finger we tied with our thumb as shown below.

[Insert April18_7]

### April 19
We finished connecting all the fingers with the strings necessary and were able to contract the fingers properly.

[Insert April19_2]

We also mapped the flex sensors to each individual servo. We have 5 of them (TowerPro SG92R). 

[Insert April19_3]

## Week 3

### April 25

[Insert April25_1]

It was now time to attach the motors to the hand and be able to control the prosthetic with the glove.

We used a 3D pen (AIO Robototics) to design the model for the forearm. 

[Insert April 25_2]

Here is a timelapse of the first half of the model being printed by hand.

[Insert April25_7]

Additionally, we started working on translating our circuits to a protoboard. First we started witht the glove's circuit. We went from this:

[Insert April25_4]

to this:

[Insert April25_5]

What the circuit for the glove does is it has 5 voltage dividers that are connected to individual analog in pins on the mBed. From there we read in the values of the flexing and standardize them to a value from 0-100. Once that is done, we send the data in a specific format to the prosthetic hand's mBed. In the protoboard, we added two additional components, one for power so that it is easy to connect a battery and a diode so that the circuit is not fried in case the battery is oriented the wrong way.




