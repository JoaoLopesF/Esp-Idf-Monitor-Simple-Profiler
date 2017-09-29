#ESP-IDF Monitor - Simple profiler

## Update of IDF Monitor to give a simple profiler output

## Contents
 - [About](#about)
 - [Wishlist](#wishlist)
 - [Releases](#releases)

## About

I needed to make a simple profiler for my project,
so I modified idf_monitor.py for this.

It's very simple, I read the time in micros at the beginning of each line,
calculate and show the difference between the time of the line and the time of the previous line
and display this in greeen, yellow or red.
There is an parameters in line 276:
[code]
self.PROFILER_MIN_MICROS_GREEN  = 0   # if the time is equal or greater this, show profiler in green
self.PROFILER_MIN_MICROS_YELLOW = 50  # if the time is equal or greater this, show profiler in yellow
self.PROFILER_MIN_MICROS_RED    = 250 # if the time is equal or greater this, show profiler in red
[/code]

This was very useful for me, because my project was generating a lot of debugging, and with this profiler it became easier to identify the bottlenecks

Follow the file idf_monitor.py, just go to $IDF_PATH/tools, rename the original file and copy the new idf_monitor.py

I hope it's useful

## Wishlist
- Make a keyboard shortcuts to enable/disable the profiler

## Releases
#### 1.0.0
- First version
