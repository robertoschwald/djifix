# djifix

Mirror of http://live555.com/drones/DJI-Phantom-2-Vision+-video-fix/

A C program to repair corrupted video files that can sometimes be produced by DJI quadcopters.

Current Version: 2018-02-21
  
## Compile

Prerequisites:
* C Compiler (LLVM / XCode in OSX, gcc in other envs)
* ffmpeg

```bash
make
make install
```

## Usage
djifix generates H264 videos. Therefore you need a tool to convert the H264 video to MP4, like ffmpeg.

```bash
djifix path/to/crashed/dji/video.[mov|mp4]
ffmpeg -i DJI_XYZW-repaired.h264 -c copy DJI_XYZW-repaired.mp4
```

