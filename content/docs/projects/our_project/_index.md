---
title: Our project name
type: docs
---

# The project name

## Abstract

After a short ideation process, in which we considered multiple ideas for our Chindōgu, we decided on implementing a device that helps you get a fire going. The goal of this device is to keep you awake while doing it by playing a sound everytime you try to close the bellows.

## Introduction

Our first sketch and also idea was to use a car horn which is powered by a battery, using laser sensors to measure the distance, see sketch below.

{{< figure src="sketch.png" caption="*First sketch of the *">}}

A detailed description of the concept and sketches of the planned implementation.

If a section grows too large or handles a very specific part of the project it can be put into [subpages]({{< ref "subpage_1#how-to-format" >}}).

{{< figure src="get_in.jpg" caption="*A drawing by David Shrigley.*">}}

## Related work 

References to related concepts, projects, books, websites, stories, systems, fruits, etc. and their relation to the project at hand.

## Implementation 

A detailed description of your prototyping process.

### Iteration №1

Tested sound ouptput by using just an arduino uno extension which could read sd cards on which we had sounds. It did not work.

### Iteration №2

Tested sound ouptput by using the arduino uno extension which could read sd cards on which we had sounds again. But now with an amplifier, also did not work, therefore we ditched the sd-card-sound idea.

### Iteration №3

Tested sound output just by using an amplifier and a basic sound, which finally did work but was making a constant noise.

{{< figure src="soundTesting.jpeg" caption="*Sound ouput with speaker and amplifier*">}}

### Iteration №4

Tested sound output again now using an amplifier, a basic sound and an ultrasonic sensor. Now the sound would only be played if you were in a give range of the sensor which after a bit of struggling with the code was working properly.

{{< figure src="soundTestingWithUltraSonicSensor.jpeg" caption="*Sound ouput with speaker, amplifier and ultrasonic sensor*">}}

### Iteration №5

While for the last two iterations the amp was hooked up to a stationary power supply we needed something more portable. We then came up with the idea to put everything onto the bellows for which we then also needed a portable power supply for everything. The solution was a powerbank which we fed into a step up converter to still be able to use the amp with our sound setup.

{{< figure src="arrangementTest.jpeg" caption="*First arrangement test*">}}

### Iteration №6

For our finalised arrangement we put the arduino uno, the amplifier and step up converted all into a tiny cardboard box and then glued it onto the bellows. We then glued the speaker and sensors onto the, before agreed on, positions as you can see in View 1 and fixated the power bank on the other side of the bellows with ducktape, see View 3.
{{< figure src="finalVer1.jpeg" caption="*Final arrangement - View1*">}}
{{< figure src="finalVer2.jpeg" caption="*Final arrangement - View2*">}}
{{< figure src="finalVer3.jpeg" caption="*Final arrangement - View3*">}}

## Conclusion

A reflection on your prototyping process and the project outcome. What happens to the prototype after the project?