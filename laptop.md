## Business Series

1. HP - Elitebook
2. DELL - Latitute
3. Lenovo - Thinkpad

## Check graphics, bios date and many more

Type "run" in search box, then select "run" and enter

```
dxdiag
```

## Check laptop model

Type "system information" & select it

```
system information
```

## [Check Laptop Battery Health & other Detail](https://www.youtube.com/watch?v=8C0MKaIR-EE)

Open "cmd" as administrator & type

```
powercfg /batteryreport
```

Then see/find and calculate

Battery health = (Full charge capacity/design capacity)

ex.

Design capacity: 41,440
Full charge capacity: 27,942

Battery health = 27,942/41,440
               = 0.67427....
That mean your battery have 67% health from actual 100% health.


## Some Minimum Requirement

1. (Minimum) dual core processor. quad core processor will be better. The more core the better
2. (Minimum) processor frequency 2.5 GHz to up
3. (Minimum) display - Full HD & display size 14 inch
4. (Minimum) Screen resolution 1920 x 1080 
5. Minimum 3 USB ([3.0 version better](https://www.youtube.com/watch?v=8gnCZUjJLhU)) port. If USB port is gray then it's 2.0 version. If it's blue then it's 3.0 version
6. (Minimum) 4GB graphic card
7. (Minimum) 256GB SSD
8. (Minimum) 8 GB DDR4 RAM. RAM frequency minimum 2400MHz speed.
9. Processor clock speed or frequency minimum 3 GHz

## Check RAM frequency, type, CAS latency and other

Download CPU-Z

https://www.cpuid.com/downloads/cpu-z/cpu-z_2.01-en.exe

In CPU-Z, you'll be able to see (in memory tab) ram type, speed, cas latency.

Check ram speed using cmd
```
wmic memorychip get devicelocator, speed
```
This cmd will return all your ram and their speed

[A quick calculation when buy ram.](https://www.youtube.com/watch?v=fym817j0vDU)
<pre>
cal = (cas latency/speed) 
    = (15/2133)
    = 0.007032.....
    = 0.007032..... * 2000 (optional calculation)
    = 14.064.....
</pre>
So, the result the lower the better

## Check processor frequency
```
wmic cpu get name, maxclockspeed, currentclockspeed
```

## Check screen resulation

1. (Way) On your windows display (welcome screen) right click & click "Display Settings". Then you will be able to see screen resulation.

2. (Way) Type "run" in search box, then select "run" and enter
    ```
    dxdiag
    ```
    Go to "Display" tab scrool down & you'll be able to see screen mode (which mean creen resulation)
3. (Way) Using CMD
```
wmic path Win32_VideoController get CurrentHorizontalResolution,CurrentVerticalResolution
```

## Check **webcam** Online

Windows 10 have buildin camera app. just type camera in type box.

https://webcamtests.com/

## Check **keyboard** online

https://en.key-test.ru/

## HDD / SSD & Temparature history check

https://www.hdsentinel.com/download.php

## Monitor display check for spots

https://testmyscreen.com/

## Sound
Laptop have buildin mouth speaker. Download & try recording

(Way) Check speaker
1. Right click on right side speaker icon & click on "Sounds". 

2. Then select "Speaker". 
3. Then left bottom corner select "configure" & then test the speaker. 
4. If sound is not clear then there have problem with speaker.

(Way) Check recording:
1. Goto "Recording" tab then speak. if microphone up-down on speak then microphone may be ok.

Also try record and then listen to be confirm.

NCH recorder
https://www.nch.com.au/software/voxrec.html



