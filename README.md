# ffmpeg_win64_with_nvenc_hwacc
FFmpeg 3.1 compliled with NVIDIA hardware acc
Config:
./configure --toolchain=msvc --target-os=win64 --arch=x86_64 --enable-nvenc --enable-hwaccels --enable-gpl


use ffmpeg -h encoder=h264_nvenc- to see profiles and presets
use ffmpeg -i input.avi -c:v h264_nvenc -preset fast -profile:v baseline output.mp4- to convert video


See https://trac.ffmpeg.org/wiki/HWAccelIntro
