# VEST: Video Event Segmentation Tool

The Video Event Segmentation Tool (VEST) is an open-source software for annotating temporal events in video clips.

You can annotate event "segments" with start & end times or event "points" that indicate only the start time of an event.

# Basic instructions
1. Installation 
Easiest way to use VEST is through the online app at [https://jinhyuncheong.com/vest/vest.html](https://jinhyuncheong.com/vest/vest.html). Alternatively, you can clone this repo and launch `index.html` in your browser. 

2. How to use
- Load your video file using the [Choose file] button
- Define the name of the event segments and points using the [Add segment buttons] and [Add point buttons]. This will create buttons with your event names on them.
- Click your label buttons to annotate segments or events as you watch your video.
- When you are finished, save your annotations by using the [Download results] button.

# Screenshot
![Screenshot of VEST in action](paper/Figure1.png?raw=true "Screenshot of VEST in action.")

# License
VEST uses [peaks.js](https://github.com/bbc/peaks.js/) and abides by its [license](https://github.com/bbc/peaks.js/blob/master/COPYING).
