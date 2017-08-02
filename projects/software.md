---
layout: post
title: 'Software'
---

While the electrical and mechanical components of the Magic School Bot are important, software is also needed to tell the robot what to do. In addition to the expected control software, we also had software to read and digitally filter IR signals instead of building an electronic IR filtering circuit. Software management was done on Github to let us work on issues concurrently.

#### Decision Making

The decision-making algorithm was organized into three stages: gate, pickup, and zipline. During the gate stage, the magic school bot followed tape until the IR signal was detected. It then waited for the signal to change to 1kHz before proceeding through the gate. During the pickup state, it followed tape until an intersection was detected, and then drove around the agent holding tank and initiated the claw sequence to retrieve the agents. Finally, the zipline stage located the zipline and transferred the basket with agents to the zipline.

|![code hiearchy]({{ site.url }}/assets/img/projects/software/code hiearchy.png)|
|:---:|
|*Our software architecture*|

<br>
This software structure was beneficial because it allowed us to write, test, and the different stages concurrently, which saved us some time.

#### Digital IR Filtering

[something something]
