---
layout: post
title: "sauron the all-seeing"
date: 2013-10-13 21:33
comments: true
categories: [research,computer vision,3D printing,prototyping]
---

My second paper is now officially published!

<img src="http://valkyriesavage.com/images/sauron.png" width=100%>

The big idea of this paper was using computer vision inside 3D printed prototypes to do the sensing (and to avoid using electronics).  First, a story.

3D printers are taking the prototyping world by storm.  Their function is to take 3D models and transform them into physical objects; this means that getting a very precise version of a prototype is fast, (reasonbly) cheap, and simple.  The unfortunate problem is that the way people *use* these 3D printers is not any different than their use of woodworking tools or their own hands.  While the designs can be more complicated, when a designer (or maker) is creating an interactive device--say a video game controller--, he still prints the model, then cuts it apart and inserts electronics (to make the joysticks and buttons work), and puts it back together.

Now, 3D printers aren't in general capable of printing electronics (yet).  What they *are* good at creating is mechanisms.  The thing is that mechanisms without electronics are hard to sense.  One good way of sensing when a mechanism is moving, however, is to watch it.  Computer vision has been successfully used by many prototyping tools to accept user input on prototype objects, and it offers a lot of power when a designer needs to track visible interactions.

You may know Sauron from the Lord of the Rings as the Dark Lord of Mordor whose great, burning eye could see happenings all across the land.  We wanted to bring Sauron's all-seeing nature to computer vision.  Computer vision has long suffered from many problems related to occlusion.  If you mount a camera above the prototype, it can't see through your hands.  You can mount many and triangulate, but this is complex and also requires a dedicated testing space for prototypes.  We decided to instead insert a single camera into the printed prototype.  To combat occlusion issues, we perform interior modifications of the prototype to bring all mechanical motion into the camera's view.  This means extending some components, and placing mirrors to see others.  The details of what we did are in the paper.

The output of this research project was a Solidworks plugin (Solidworks is a commercial CAD tool used by professional mechanical engineers for their design work).  I can't say that it's as fast or efficient as it could be, however the idea and approach are the important thing, and I hope to see something similar available in more accessible tools in the future!  Our tool basically provides the designer with a virtual camera that matches the field of view of his physical camera.  He inserts it into his design where he plans to attach the physical camera post-print, and the tool performs some modifications so that all components are visible.  We supported buttons, sliders, joysticks, direction pads, dials, scroll wheels, and trackballs, but the library is extensible and any component could be added.  We toyed with ideas about creating a trackpad (simple to do, since plastic is translucent and fingers' shadows can be tracked through thin layers of it), accelerometer (by suspending a weight attached to 3 chains inside the prototype, we can sense the orientation of the device), and other sensors, but I'm mostly excited to see what other people think up!
