## ESP-IDF Monitor - Simple profiler

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

    self.PROFILER_MIN_MICROS_GREEN  = 0   # if the time is equal or greater this, show profiler in green
    self.PROFILER_MIN_MICROS_YELLOW = 50  # if the time is equal or greater this, show profiler in yellow
    self.PROFILER_MIN_MICROS_RED    = 250 # if the time is equal or greater this, show profiler in red

This was very useful for me, because my project was generating a lot of debugging, and with this profiler it became easier to identify the bottlenecks

Have 2 versions of monitor with simple profile
- esp-idf-v3.0 -> to use in v3.0.* of Esp-Idf
- esp-idf-v3.1 -> to use in v3.1.* of Esp-Idf

To install, just download the file idf_monitor.py, just go to $IDF_PATH/tools, rename the original file and copy the new idf_monitor.py

I hope it's useful

## How it looks

![Imgur Image](https://i.imgur.com/ZVCQENq.png)

Obs: the "P(nnn)" is a profiler, where nnn is a time in microseconds elapsed

## Wishlist
- Make a keyboard shortcuts to enable/disable the profiler

## Releases
#### 1.0.0
- First version
#### 1.0.1
- Update v3.0 idf_monitor.py
- New v3.1 beta idf_monitor
