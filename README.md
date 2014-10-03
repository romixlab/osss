osss
====

Open Source Surveillance System

For now it's just a draft. I decided to create this sytem because I don't know any open source system with described capabilities (there is some proprietary solutions, but you can't extend them in any way).

Concepts
--------
Everything is a module! In the picture below capture process for an IP camera are shown. Two video capture modules receives h.264 and mjpeg streams from camera and third receive audio stream. Then each module places captured data to ring buffers that are accessible by other modules. Some modules may also decode recieved data and place it in another buffer for ruther processing
([[images/capture.jpg]])
Capturing h.264 and mjpeg stream in parallel could improve performance - h.264 have a bigger compression ratio than mjpeg. So decoding mjpeg is easier than h.264, while writing h.264 stream to an archive is more space efficient.


You can watch draft file in [yEd Graph Editor](http://www.yworks.com/en/products_yed_about.html)

I would be very happy to hear any thoughts about osss!
