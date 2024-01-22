---
title: Our project name
type: docs
---

# Franz the frenzy

## Abstract

After a short ideation process, in which we considered multiple ideas for our Chindōgu, we decided on implementing a device that helps you get a fire going. The goal of this device is to keep you awake while doing it by playing a sound everytime you try to close the bellows.

## Introduction

Our first sketch and also idea was to use a car horn which is powered by a battery, using laser sensors to measure the distance, see sketch below.

{{< figure src="sketch.png" caption="*First sketch of Franz*">}}

The task at hand was to make a Chindōgu, a concept not too foreign to us. We'd seen pictures of Chindōgus before, we just hadn't heard the name of the concept. Throughout our idea-finding-phase we kept looping
back to a very annoying, multi-functional bellow. Why would one need such a device? That is the wrong question to ask, for we made one anyway. A bellow to stand above them all, with both sound effects to
scare away wild animals and a flashlight to find things in the night. The plan was to make the sounds primarily come from the user opening and closing the bellow itself, while the flashlight should've been toggleable. The twists to make it less useful were to make the sound so annoying that you wouldn't want to use it, even if there was a wild animal approaching and to make the flashlight really, really not fit for the job. How did we accomplish this? You'll find that out throughout this paper.

## Related work 

It was quite the challenge to find anything related to our work at all, as projects with bellows were few and far between. And while we didn't take our inspiration from works including bellows, we still had some very
strong influences. The YouTube channel "I did a thing", which specializes in making completely unnecessary and (sometimes) pointless changes to simple things, was probably the greatest.

{{< figure src="i_did_a_thing.png" caption="*\"I made the worlds most dangerous pool stick\" by I did a thing*">}}

Another great creator that comes to mind and inspired us was "Unnecessary Inventions", which, as the title of the channel suggests, focuses on inventing stuff with superbly limited use cases (if any). It was a great help to think outside the box about useless and humorous features which we wanted to add.

{{< figure src="unnecessary_inventions.png" caption="*\"11 ABSURD Inventions I built that absolutely noone needs\" by Unnecessary Inventions*">}}

## Implementation 

### Basic Components gathering
We got started with testing out different parts of the projects individually and looked for expected flaws in our initial design aspects.
Our first idea was to get a car horn to play a "HONK" every time you use the bellow. That proved to be difficult, since the power supply would have to be rather large and we would need to use a converter to increase the voltage from 5V arduino output to much much more.

### Changing our way of audio implementation
So, we scrapped the idea of the car horn and tried using an audio speaker. This little downgrade was to be expected and we quickly got down to testing. Since the power supply remained uncertain, we looked for a little speaker which required a low amount of voltage - alas it didn't.

### We need more power
Back to the drawing board, we had to figure out our power situation. In the end we used a power bank to supply the arduino with constant voltage and a - for now externally powered - audio amplifier to get the speaker to work properly. With this setup, we were able to make sounds and also adjust the volume according to the amplifier's adjuster.

### To measure - or not to measure
The next step consisted of setting up our distance sensor. Our original plan has been to use
a laser-based distance sensor. We also quickly scrapped that idea - simply because our
professors already had an ultrasonic sensor at hand that we could use instead. We tested
the sensor's capabilities and got it to work properly for our purpose.

### The last piece of the puzzle
Finally, we had most of the components figured out.
A power bank as power supply, a distance sensor to trigger our arduino script, an amplifier to get our speaker to make a sound and the speaker itself. One component was missing in that equation - which was the still externally powered amplifier. To solve even the last issue, we used a step-up converter, to get the needed 12V for the amplifier to work properly. That's it, the components worked individually, the design was flawless and we were eager to
build the thing!

### Materials used
<ul>
<li>Power bank as power supply</li>
<li>Ultrasonic sensor HC-SR04</li>
<li>Step-up converter MT3608 (5V to 12V)</li>
<li>"battered" audio speaker</li>
<li>Audio amplifier board Class D</li>
<li>A bellow (purchased at OBI)</li>
<li>some tape and love</li>
<li>wires and zinc for soldering</li>
</ul>

#### Iteration №1

Tested sound ouptput by using just an arduino uno extension which could read sd cards on which we had sounds. It did not work.

#### Iteration №2

Tested sound ouptput by using the arduino uno extension which could read sd cards on which we had sounds again. But now with an amplifier, also did not work, therefore we ditched the sd-card-sound idea.

#### Iteration №3

Tested sound output just by using an amplifier and a basic sound, which finally did work but was making a constant noise.

{{< figure src="soundTesting.jpeg" caption="*Sound ouput with speaker and amplifier*">}}

#### Iteration №4

Tested sound output again now using an amplifier, a basic sound and an ultrasonic sensor. Now the sound would only be played if you were in a give range of the sensor which after a bit of struggling with the code was working properly.

{{< figure src="soundTestingWithUltraSonicSensor.jpeg" caption="*Sound ouput with speaker, amplifier and ultrasonic sensor*">}}

#### Iteration №5

While for the last two iterations the amp was hooked up to a stationary power supply we needed something more portable. We then came up with the idea to put everything onto the bellows for which we then also needed a portable power supply for everything. The solution was a powerbank which we fed into a step up converter to still be able to use the amp with our sound setup.

{{< figure src="arrangementTest.jpeg" caption="*First arrangement test*">}}

#### Iteration №6

For our finalised arrangement we put the arduino uno, the amplifier and step up converted all into a tiny cardboard box and then glued it onto the bellows. We then glued the speaker and sensors onto the, before agreed on, positions as you can see in View 1 and fixated the power bank on the other side of the bellows with ducktape, see View 3.
{{< figure src="finalVer1.jpeg" caption="*Final arrangement - View1*">}}
{{< figure src="finalVer2.jpeg" caption="*Final arrangement - View2*">}}
{{< figure src="finalVer3.jpeg" caption="*Final arrangement - View3*">}}

## Conclusion

It was a pretty fun experience overall. We had a chance to look at electrical engineering in a bit more detail and with helping hands and a few ropes we pulled it off.

At the ideation process of all the teams, we heard some pretty nice ideas to try ourselves in the near future. Since we learned that most of the awesome components we use in our everyday lives were often built in little step-by-steps and large amounts of prototypes, it inspired some of us to keep at it and figure out solutions for our homes and places ourselves.

We also learned a lot from other teams and their problems while building.
Power supply knowledge, soldering stuff together, where to buy stuff cost efficiently and all the different approaches to problems.

### What happens with the prototype?
Well, it will be remembered as our first bigger step in building stuff on our own and it helped us to improve our problem solving. Not everything has to be bought from a big supplier - we also have custom problems and therefore are now better able to solve them ourselves.

TL;DR: It will be ripped apart again and the parts will be sent back to the professors to
educate the next students, like they did with us.

5 star rating for this course - can only recommend it!