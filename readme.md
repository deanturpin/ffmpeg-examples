### Rotate a video
```
ffmpeg -ss 79 -i VID_20160917_183404.mp4 -t 3.75 -r 24 -y -vf 'rotate=PI' hs.gif
```

### Prepare MP3 for YouTube
``` bash
ffmpeg -loop 1 -r 1 -i pic.jpg -i audio.mp3 -c:a copy -shortest output.avi
```

From (superuser)[http://superuser.com/questions/700419/how-to-convert-mp3-to-youtube-allowed-video-format].
