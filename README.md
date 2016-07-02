# ffmpeg_win64_with_nvenc_hwacc
FFmpeg 3.1 compliled with NVIDIA hardware acc


-------------------------------------------------
quote from https://trac.ffmpeg.org/wiki/HWAccelIntro
-------------------------------------------------
NVENC is an API developed by NVIDIA which enables the use of NVIDIA GPU cards to perform H.264 and HEVC encoding. FFmpeg supports NVENC through the nvenc_h264 and nvenc_hevc encoders. In order to enable it in FFmpeg you need:

A supported GPU
Supported drivers
Locally installed nvEncodeAPI.h header files from the NVENC SDK
ffmpeg configured with --enable-nvenc
Visit ​NVIDIA Video Codec SDK to download the SDK and to read more about the supported GPUs and supported drivers.

Usage example:

ffmpeg -i input -c:v nvenc_h264 -profile high444p -pixel_format yuv444p -preset default output.mp4
You can see available presets, other options, and encoder info with ffmpeg -h encoder=nvenc_h264 or ffmpeg -h encoder=nvenc_hevc.

Note: If you get the No NVENC capable devices found error make sure you're encoding to a supported pixel format. See encoder info as shown above.
-------------------------------------------------
