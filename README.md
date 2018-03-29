# djifix

Mirror of http://live555.com/drones/DJI-Phantom-2-Vision+-video-fix/

A C program to repair corrupted video files that can sometimes be produced by DJI quadcopters.

Current Version: 2018-02-21 (2018-01-27)
  
## Compile

Prerequisites:
* C Compiler (LLVM / XCode in OSX, gcc in other envs)
* ffmpeg
* VLC viewer (optional, to check the repaired h264 video)

```bash
make
make install
```

## Usage
djifix generates H264 videos. Therefore you need a tool to convert the H264 video to MP4, like ffmpeg.

```bash
djifix path/to/crashed/dji-video.[mov|mp4]
ffmpeg -i dji-video-repaired.h264 -c copy dji-video-repaired.mp4
```

The program asks for the video format. You must try different versions. You can check the repaired h264 video in the VLC viewer. 
For example a DJI Mavic Drone recorded video in 1080p was successfully repaired using Video Mode 1080p, 60fps (Option "B").
