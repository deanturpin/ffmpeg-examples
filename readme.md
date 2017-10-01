# Rotate
```ffmpeg -ss 79 -i VID_20160917_183404.mp4 -t 3.75 -r 24 -y -vf 'rotate=PI' hs.gif```

# Reverse
```ffmpeg -i REC00019.AVI -vf reverse rev.mp4```

# MP4 to looped GIF
```ffmpeg -i blah.mp4 -loop 0 looped.gif```

# Prepare MP3 for YouTube
```
ffmpeg -loop 1 -r 1 -i pic.jpg -i audio.mp3 -c:a copy -shortest output.avi
```

From [superuser](http://superuser.com/questions/700419/how-to-convert-mp3-to-youtube-allowed-video-format).

# Swap the audio on a video
Specify audio first. Includes offset and write to a MOV as WhatsApp doesn't recognise AVIs.

```
ffmpeg -i audio.mp3 -i video.mov -shortest new.mov -y
ffmpeg -i audio.mp3 -i video.mov -vf reverse -shortest new.mov -y
```
