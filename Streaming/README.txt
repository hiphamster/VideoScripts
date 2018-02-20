This folder contains scripts for helping you live stream to sites like Twitch, YouTube, and Picarto.

Scripts:
    * StreamPi --> Stream to RTMP supported services like Twitch, YouTube, Picarto, etc.
        1. If saving screen capture session as a recording use:
                /path/to/StreamPi [output.flv]
        2. If streaming live to Twitch, YouTube, Picarto, etc. via RTMP use:
                /path/to/StreamPi [rtmp://...]
        3. You can save yourself some time by creating aliases in $HOME/.bashrc
           or by adding your RTMP URL in the RTMP variable inside of the script
           itself.