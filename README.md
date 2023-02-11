# kunitaka-photo-1

## 動画加工

### 動画分割

```sh
ffmpeg -i IMG_6275.MOV -map 0 -c copy -f segment -segment_time 60 -reset_timestamps 1 IMG_6275_%02d.MOV
```

### 動画から静止画

```sh
video2jpg
```
