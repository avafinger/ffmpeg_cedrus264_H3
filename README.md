# FFmpeg - H3 platform (Cedrus HW Encoder - CMOS Camera)

FFmpeg with built in Cedrus264 HW Encoder for the H3 platform.
This was build on Armbian and rootfs Ubuntu 14.04


Dependencies
============

	libx264
	libv4l2
	libpulse
	libmp3lame
	libv4lconvert
	libjson-c
	libpulsecommon-4.0
	libjpeg
	libFLAC
	libvorbisenc
	libvorbis
	libogg


Source Code
===========

https://github.com/uboborov/ffmpeg_h264_H3


How to use it
=============

- Attach you CMOS camera
- Clone the repo: git clone https://github.com/avafinger/ffmpeg_cedrus264_H3.git
- cd ffmpeg_cedrus264_H3
- type: 

	sudo ./ffmpeg -f v4l2 -channel 0 -video_size 640x480 -i /dev/video0 -pix_fmt nv12 -r 30 -b:v 64k -c:v cedrus264 test.mp4

Play the MP4 file with your preferred application

Limitations
===========
 * Read the author notice 
