This folder contains scripts for helping you live stream to sites like Twitch, YouTube, and Picarto.

Scripts:
    * StreamPi --> Stream to RTMP supported services like Twitch, YouTube, Picarto, etc.
      This script is technically designed for a Raspberry Pi 3, but has also been tested
      on older i686 laptops, the point being to have a modest OBS Studio alternative.
        1. If saving screen capture session as a local recording use:
                /path/to/StreamPi [output.flv]
        2. If streaming live to Twitch, YouTube, Picarto, etc. via RTMP use:
                /path/to/StreamPi [rtmp://...]
        3. If using a transparent (RGBA) image as an overlay:
                /path/to/StreamPi [rtmp://...] /path/to/RGBA_image
        4. You can save yourself some time by creating aliases in $HOME/.bashrc
           or by adding your RTMP URL in the RTMP variable ($1) inside of the script
           itself.
        5. Work-flow:
                a. Checks if you wanted an overlay image based on a variable ($2)
                b. Grabs the screen/monitor width and height
                c. If you want an overlay image, resize a copy of the image to match screen 
                   resolution.
                d. Checks a variable to see if you want multiple monitor (spans width) recording.
                   The default is set to "N" for "no" to only stream/record the primary display.
                e. Checks whether or not you are using a Raspberry Pi or running JACK to choose
                   the appropriate sound server (ALSA, Pulse, JACK).
                f. Based on screen/monitor resolution, it will choose whether or not to scale
                   the stream/recording to 720p. This is to help the Raspberry Pi have a better
                   framerate on 1080p monitors. You can change this value if you'd like and 
                   probably should if you are running this on a newer x86_64 laptop/desktop.
        6. For video demonstration: https://www.bitchute.com/video/2yWzuFMUaBra
