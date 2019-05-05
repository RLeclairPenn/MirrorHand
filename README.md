# This is Mirror Hand!
### By: Rafael Gerkhe and Raul Leclair

Currently available prosthetics are either completely mechanical, with limited independent movement between joints, or costs thousands of dollars and require surgery to create an interface between nerves and the system. **Mirror Hand** proposes a way of improving low-cost prosthetics in cases where the user has an able hand, so that we can have it control the movements of the prosthetic. Therefore, adding functionality to the prosthetic by giving greater control over the prosthetic fingers to the user. 

If you would like to see the videos we prepared for our demo:

Rafael forgetting his Wawa Bag: https://www.youtube.com/watch?v=0YRK3EDscS8

Opening a glue bottle: https://www.youtube.com/watch?v=HV1luiP_14o

Rafael hydrating: https://www.youtube.com/watch?v=bbDRLOT-rF0



## Week 1 

### April 10

We started constructing the glove which will have the flex sensors (SparkFun SEN-10264) that will give us the position of the able hand's fingers in order to translate them to a prosthetic. So far we have sewed the flex sensors into a glove.

<img src="April10_1.jpg" width="200" />

We connected the sensors to a multimeter to measure the resistance and check if it changed when we flexed which it did.

<img src="April10_2.jpg" width="200" /> 

and 

<img src="April10_3.jpg" width="200" />

We learned that flex sensors are not entirely flexible when all five of the flex sensors we had broke. The reason they broke being that one of the "flexible" parts is not supposed to be flexed and if it is flexed there is a risk that the thin metallic sheet is broken as shown below. 

<img src="April10_5.jpg" width="200" />

### April 11

With the flex sensors broken, we had to disarm the glove entirely. Luckily for us we had an extra flex sensor. We used the following equation to be able to calibrate the sensor on the range of 0-100 for better use. 

<img src="April11_1.jpg" width="200" />

## Week 2

### April 18
The flex sensors arrived and we secured the place at which they could break with shrink wrap so that they stayed solid. We sewed and glued them to the hand and we got the readings we needed.

Over the weekend we printed the open-source prosthetic hand (https://www.thingiverse.com/thing:596966) which ended up being somewhat smaller than we predicted. 

<img src="April18_1.jpg" width="200" />

Nonetheless, we assembled it and started tying the strings to the fingers. We used some flexible string we bought and yellow cord from Detkin.

<img src="April18_2.jpg" width="200" />

Once one of the fingers was tied up we attached it to a servo and had it flex and unflex the finger.

[Insert April18_4]

Additionally, we set up the bluetooth modules (HC05) to communicate exclusively with each other. We connected them to two different mBeds and had them communicate. Once we were able to send messages in between the mBeds we started sending the data from the glove to the mBed that would control the prosthetic. We were succesful in doing so and were able to control the one finger we tied with our thumb as shown below.

[Insert April18_7]

### April 19
We finished connecting all the fingers with the strings necessary and were able to contract the fingers properly.

<img src="April19_2.JPG" width="200" />

We also mapped the flex sensors to each individual servo. We have 5 of them (TowerPro SG92R). 

<img src="April19_3.JPG" width="200" />

## Week 3

### April 25

<img src="April25_1.jpg" width="200" />

It was now time to attach the motors to the hand and be able to control the prosthetic with the glove.

We used a 3D pen (AIO Robototics) to design the model for the forearm. 

<img src="April25_2.jpg" width="200" />

Here is a timelapse of the first half of the model being printed by hand.

<img src="April25_7.jpg" width="200" />

Additionally, we started working on translating our circuits to a protoboard. First we started witht the glove's circuit. We went from this:

<img src="April25_4.JPG" width="200" />

to this:

<img src="April25_5.JPG" width="200" />

What the circuit for the glove does is it has 5 voltage dividers that are connected to individual analog in pins on the mBed. From there we read in the values of the flexing and standardize them to a value from 0-100. Once that is done, we send the data in a specific format to the prosthetic hand's mBed. In the protoboard, we added two additional components, one for power so that it is easy to connect a battery and a diode so that the circuit is not fried in case the battery is oriented the wrong way.

With the protoboard done, we attached it to the glove to get the final version which is shown here:

<img src="April25_14.jpg" width="200" />

We also attached the servos to the printed forearm so it would look something like the following (mind this only has one servo):

<img src="April25_6.jpg" width="200" />

As we tested the servo we realized that the yellow string was too thick to work properly and it caused to much friction in between the components. We decided to change the yellow string to nylon and connected the nylon to each of the servos. An example connection is shown below.

<img src="April25_8.jpg" width="200" />

To test the connection we just attached one servo to only one finger and tested to see if it worked properly. Once it did we continued on to the next fingers. Below is a sample of one of the fingers working.

[Insert April25_10]

With that done, we attached all of the servos to the prosthetic hand and properly mapped the fingers. With some testing and calibration we achieved the following results:

Insert[April25_11]

We also translated the circuit for the prosthetic into a protoboard which is shown below:

<img src="May01_1.jpg" width="200" />

<img src="May01_2.jpg" width="200" />

The circuit here is the final version of the prostethic's circuit. It contains 5 voltage regulators (one is underneath the mBed) that regulate the voltage outputted by the battery to the servos. The servos are connected to pins that have an output to regulate how much they have to move. Beneath the mBed there is also the bluetooth (HC05) device to communicate. There is also the pins to connect the battery and a diode to prevent reverse current. Later on we added the button and potentiometer. 

Once we connected the protoboard we achieved the following:

We managed to grab a semi crushed can of soda:

Insert[April25_12]

We also managed to grab a charger:

[Insert April25_13]

### April 26
After adjusting some of the strings, adding rubber bands and silicone to the prosthetics finger tip and added a button that freezes the hand in position we accomplished the following:

[Insert April26_5]

## Week 4

### April 30

Now that the mirror hand is basically completed, we added a handle to the prosthetic so that it is easier to demo. We also attached the prosthetic's protoboard to the forearm. Additionally we added and tested the potentiometer which based on how much resistance it is outputting will delay the freezing of the hand when the button is pressed. Basically, it is a timer that is activated when the button is pressed. When the timer is over the hand is frozen. We also made the glove have longer cables to provide more comfort to the wearer.

The final model of the prosthetic:

[Insert FinalProsthetic]

The final model of the glove:

[Insert FinalGlove]

The use of the potentiometer can be viewed in the demo videos at the start of this blog (the summary).


