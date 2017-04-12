# ekspres

```
ffprobe video_orig.mp4
identify img_60%.png

convert img_crop_257x457.png -resize 50% img_129x229_50%.png

img_w=131 img_h=191 && vid_w=320 && vid_h=360 && ffmpeg -i video_orig_320x360.mp4 -i img_60%_131x191.png  -i sr_logo_200x25.png -filter_complex "overlay=x=$(echo $vid_w-$img_w):y=$(echo $vid_h-$img_h-20) [tmp];[tmp] overlay=40:0" result_sr.mp4

```
