# utl-capturing-old-faithful-before-and-during-an-eruption--AI-visual-analytics
Capturing old faithful before and during an eruption  AI visual analytics
    Capturing old faithful before and during an eruption  AI visual analytics

    Saving frames from webcam stream AI visual analysis

    There are three geysers in the webcam old faithful is the rightmost

    20 minutes before eruption
    https://tinyurl.com/yd8wt9oe

    10 minutes before eruption
    https://tinyurl.com/yaf22qfr

    Eruption
    https://tinyurl.com/yd5mmq36

    github
    https://tinyurl.com/y8hvr6pf
    https://github.com/rogerjdeangelis/utl-capturing-old-faithful-before-and-during-an-eruption--AI-visual-analytics


    Other AI repos
    https://tinyurl.com/y8ybchhv
    https://github.com/rogerjdeangelis?utf8=%E2%9C%93&tab=repositories&q=in%3Aname+AI&type=&language=

    Setup for windows
    https://video.stackexchange.com/questions/20495/how-do-i-set-up-and-use-ffmpeg-in-windows


    StackOverflow
    https://stackoverflow.com/questions/53980367/saving-frames-from-webcam-stream

    Gyam profile
    https://stackoverflow.com/users/5726027/gyan

    INPUT
    =====

    Continuous streaming webcam

        https://www.nps.gov/yell/customcf/geyser_webcam_updated.htm

    Playlist  (need this for ffmpeg

        https://56cf3370d8dd3.streamlock.net:1935/nps/faithful.stream/playlist.m3u8


    PROCESS
    =======

    * just in case you rerun;
    %utlfkil(d:/png/olF0mn.png);
    %utlfkil(d:/png/olF1mn.png);
    %utlfkil(d:/png/olF2mn.png);

    * after ffmpeg.exe was installed;
    * takes a while to connect and get the frame;
    data _null_;
     * 20 mins before;
     x= 'ffmpeg -i https://56cf3370d8dd3.streamlock.net:1935/nps/faithful.stream/playlist.m3u8 -frames:v 1 d:/png/olF0mn.png';
     call system(x);

     * 10 mins before;
     call sleep(60,1);
     x= 'ffmpeg -i https://56cf3370d8dd3.streamlock.net:1935/nps/faithful.stream/playlist.m3u8 -frames:v 1 d:/png/olF1mn.png';
     call system(x);

     * Eruption;
     call sleep(60,1);
     x= 'ffmpeg -i https://56cf3370d8dd3.streamlock.net:1935/nps/faithful.stream/playlist.m3u8 -frames:v 1 d:/png/olF2mn.png';
     call system(x);

    run;quit;


    OUPUT
    =====

    d:/png/olF0mn.png
    d:/png/olF1mn.png
    d:/png/olF2mn.png

    Copied to

    https://tinyurl.com/yd8wt9oe
    https://tinyurl.com/yaf22qfr
    https://tinyurl.com/yd5mmq36







