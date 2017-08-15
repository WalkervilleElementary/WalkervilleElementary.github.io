---
layout: post
title: 'Software'
---

While the electrical and mechanical components of the Magic School Bot are important, software is also needed to tell the robot what to do. In addition to the expected control software, we also had software to do signal processing on IR signals. Software management was done on [Github](https://github.com/walkervilleElementary/robot) to let us work on issues concurrently.

### Decision Making

The decision-making algorithm was organized into three stages: gate, pickup, and zipline. During the gate stage, the magic school bot followed tape while keeping track of whether or not it is safe to go through the gate. If necessary it waits for the signal to change to 1kHz before proceeding through the gate. During the pickup state, it followed tape until an intersection was detected, and then drove around the agent holding tank, aligning the robot and initiated the claw sequence to retrieve the agents. Finally, the zipline stage located the zipline and transferred the basket with agents to the zipline.

<center><img src="{{ site.url }}/assets/img/projects/software/code hiearchy.png"  /></center>

<center><i>Our software architecture</i></center>

<br>
This software structure allows us to have concurrency on a single process computer. It is also beneficial because it allowed all of us to write, test, and the different stages at the same time, which saved us some time.

### Digital IR Filtering

Instead of filtering IR signals using hardware, we process the signal digitially. We sample the signal for a period of time and checks if the frequency of the waveform. This allowed us to remove the IR detector circuit from the robot design.

<br>

<div class="division">
    <div class="left" style="text-align: left"> <font size="+2"><a href="{{ site.url }}/electrical.html">< Electrical</a> </font></div>
    <div class="right" style="text-align: right"> <font size="+2"><a href="{{ site.url }}/fun.html">Fun ></a> </font></div>
</div>

<style type="text/css">
    .division {
    }
    .left {
        width = 50%;
        float: left;
    }
    .right {
        width: 50%
        float: right;
    }
</style>