# kunitaka-photo-1

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

This repository contains 3D assets of a high school, suitable for augmented reality, along with sample video processing commands.

## 3D Assets for Augmented Reality

The core of this repository is a set of 3D scans of a high school, provided in formats ready for AR development.

### AR Preview

You can preview the main 3D model in augmented reality on an iOS or iPadOS device by opening the link below. This will allow you to place and view the school building in your own environment.

- [View the high school model in AR](video/h18.usdz)

### Asset Files

The 3D models are available in the following formats:
- **`.usdz`**: For native use in ARKit on Apple platforms. Key files include `kunitaka-highschool.usdz` and additional scans from the Scaniverse app in the `threed/` directory.
- **`.glb`**: A standard format for 3D scenes. See `kunitaka-highschool.glb`.

## Video Processing Utilities

This repository also includes sample command-line snippets for video processing.

### Video Segmentation

To split a video into 60-second segments using FFmpeg:

```sh
ffmpeg -i IMG_6275.MOV -map 0 -c copy -f segment -segment_time 60 -reset_timestamps 1 IMG_6275_%02d.MOV
```

### Video to Images

To convert a video into a sequence of JPEG images (assumes a `video2jpg` script is in your path):

```sh
video2jpg
```

## License
MIT License — see [LICENSE](LICENSE).