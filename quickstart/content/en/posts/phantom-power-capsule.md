---
title: "Phantom Power Capsule"
date: 2020-08-23T17:39:57+12:00 
description: "I built a cheap and easy phantom power supply to pair with my cheap condenser microphone from AliExpress"
draft: false
hideToc: false
enableToc: false
enableTocContent: false
author: Lewis
authorEmoji: 🦉
tags: 
- Project
image: images/icons/bm800.jpeg
---

Something I like doing in my free time is catching up with my friends using VOIP software like Skype (RIP) or Discord. For years I've been using a dinky little microphone that I bought from Dick Smith (also RIP) when I was 14. Here's what it looks like:

{{< img src="/images/phantom-power/old-mic.jpg" alt="{Picture of my old microphone}" width="500px" height="375px">}}

<br/>

Now, I don't really think it's fair on my friends to have to put up with that so a while ago I bought myself a cheap BM-800 condenser microphone from AliExpress along with a microphone stand for it. I waited for it until I forgot that I was waiting for it and it showed up at my door. I plugged it into my PC ready to test it out and.. it was very, very quiet. After some research I found out that I needed to supply this type of microphone with phantom power to really get anything worthwhile out of it.

As an opportunity for learning, I decided to see how hard it would be to make my own phantom power supply and to my surprise it can be done quite simply. If you power it with batteries. I found a resource from [epanorama.net](https://www.epanorama.net/circuits/microphone_powering.html#phantom) that offers multiple different circuit diagrams and information for a hobbyist to make their own phantom power. 

I opted for the "Simplest Circuit" option listed on that website because the three main downsides that the author talks about aren't an issue for my use case scenario. Let's take a quick look at these downsides:

<br/>

1. Sensitivity to noise in phantom power

We're using batteries here, so we're dealing with a very clean DC signal for our phantom power.

2. Prone to interference

This still needs to be looked at. I haven't noticed any interference issues arising since using this setup, but some may arise. I had issues with my old microphone picking up interference signals occasionally though so I'm still going to be better off regardless.

3. High Output Impedance (can't properly drive long cables)

We aren't not using particularly long cables with this setup, I only need them to be long enough to route around my desk from my computer.

4. This circuit makes very high level popping noise when it is connected/disconnected

This microphone will be plugged in all the time.

5. This circuit loads the phantom power in very unbalanced way which can disturb some older mixers

We're not using a mixer here, just using an XLR to 3.5mm cable. Although the article goes over how to fix this issue pretty easily too.

<br/>

So after considering the downsides of using the simplest circuit and deeming them not worth worrying about, I chose to continue onwards with the simplest circuit. This means that I didn't even have to make a board and I didn't have to try and source any high quality zener diodes. 

Epanorama.net recommends a 47kΩ resistor for a 45V phantom power system. So I went to Jaycar and bought some cheap 9V batteries thinking "9*5 = 45, that should work!". I was mistaken. When I hooked the batteries up in series and attached them to my multimeter I found that they were reading closer to 40V than 45V. Testing the batteries individually showed a reading closer to 8V than 9V, so I added a sixth cell in to bring my total voltage up to around 48V. I decided to stick with the 47kΩ resistor even at 48V though, thinking that maybe the voltage in my batteries will drop over time and approach 45V and I already had a 47kΩ resistor in my box of resistors. 

Here's the circuit diagram I ended up with: 

{{< img src="/images/phantom-power/simple-circuit-diagram.jpg" alt="{phantom power circuit dia}">}}
<br/>

I built this circuit during the first lockdown in Christchurch due to COVID-19 and verified it functional. From there I began designing an enclosure to put it all in. Initially I was going to use the 3D printers available at the Christchurch Central Library, Tūranga. After going there and investigating however, I was advised to use one of their laser cutters for my enclosure instead. The staff there were really helpful to me and helped me use Adobe Illustrator to draw up some diagrams for the laser cutter - and all it cost me was a small donation! I used the generator available at (festi.info)[https://www.festi.info/boxes.py/] to get a basic box generated and then modified it to fit my needs, and had it cut.


{{< img src="/images/phantom-power/box-mid-assembly.jpg" alt="{PictureHere}" width="500px" height="375px">}}
<br/>

I didn't manage to take any pictures of it being cut, as I was having too much fun just watching it go! But it turned out really good, so I folded all the pieces togethor and glued them up with some PVA glue.

{{< img src="/images/phantom-power/box-filled.jpg" alt="{PictureHere}" width="375px" height="500px">}}

<br/>

Then I assembled my circuit, and slotted it into the box. I super glued the XLR connectors to the front and that was a lot easier than trying to laser cut screw holes for them.

{{< img src="/images/phantom-power/box-complete.jpg" alt="{PictureHere}" width="375px" height="500px">}}

<br/>

Overall, the project was a great success and my microphone sounds better than ever!


---

I have recorded a few different audio samples of the two mics and want to add them here but I still need to figure that out and it's getting late.

<audio controls>
  <source src="/sounds/phantom-power/oldmic.mp3" type="audio/mpeg">
</audio>

<br/>

<audio controls>
  <source src="/sounds/phantom-power/newmic20db.mp3" type="audio/mpeg">
</audio> 

<br/>

<audio controls>
  <source src="/sounds/phantom-power/newmicphantompower.mp3" type="audio/mpeg">
</audio> 
