# Homepage template
Playing around with various HTML5, CSS3 and JS techniques to achieve an awesome homepage. This is _experimentation_, please do not use this for anything beyond inspiration.

## Video encoding parameters
```
ffmpeg -i input-video.mp4 -c:v libvpx -crf 12 -b:v 1000k -an video.webm
ffmpeg -i input-video.mp4 -c:v libx264 -crf 19 -b:v 800k -an video.mp4
ffmpeg -i input-video.mp4 -c:v libtheora -b:v 1200k -an video.ogg
```
`ffmpeg` the encoding software - get it [here](https://ffmpeg.org/download.html) or with apt/brew  
`-i input-video.mp4` your input video  
`-c:v libvpx` the codec for the output video  
`-crf 12` constant rate factor between 0 and 51 - lower is better but larger filesize  
`-b:v 1000k` bitrate of the output video  
`-an` strip audio  
`video.webm` the output file  

Optional: `-vf scale=720:404` to scale the video. The `youtube-dl` and `mediainfo` packages are also quite handy with video operations.