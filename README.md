[![TrafficCamera_Unwarp_Image](TrafficCamera_Unwarp_Image/images/traffic.gif)](TrafficCamera_Unwarp_Image/README.md)
[![TrafficCamera_Unwarp_Image](TrafficCamera_Darknet_YOLOv3/images/yolov3.gif)](TrafficCamera_Darknet_YOLOv3/README.md)

# How to start?

Clone this repository with submodules:

Using git 2.13

```
git clone https://github.com/karolmajek/TrafficAnalysis.git --recurse-submodules
```

Using old git

```
git clone https://github.com/karolmajek/TrafficAnalysis.git --recursive
```

If you already cloned:

```
cd TrafficAnalysis
git submodule update --init --recursive
```

# Download 4K Input Video

You can use youtube-dl to download video:

```
youtube-dl -f 313 MNn9qKG2UFI
```

If you need lower resolution just change `-f 313` to one of:

```
youtube-dl -F MNn9qKG2UFI
```

```
[info] Available formats for MNn9qKG2UFI:
format code  extension  resolution note
249          webm       audio only DASH audio   46k , opus @ 50k, 1.61MiB
250          webm       audio only DASH audio   61k , opus @ 70k, 2.14MiB
251          webm       audio only DASH audio  122k , opus @160k, 4.32MiB
171          webm       audio only DASH audio  127k , vorbis@128k, 4.35MiB
140          m4a        audio only DASH audio  128k , m4a_dash container, mp4a.40.2@128k, 4.64MiB
278          webm       256x144    144p   98k , webm container, vp9, 30fps, video only, 3.45MiB
160          mp4        256x144    144p  117k , avc1.4d400c, 30fps, video only, 2.99MiB
242          webm       426x240    240p  224k , vp9, 30fps, video only, 7.03MiB
133          mp4        426x240    240p  265k , avc1.4d4015, 30fps, video only, 6.71MiB
243          webm       640x360    360p  415k , vp9, 30fps, video only, 13.91MiB
134          mp4        640x360    360p  445k , avc1.4d401e, 30fps, video only, 10.76MiB
244          webm       854x480    480p  763k , vp9, 30fps, video only, 26.28MiB
135          mp4        854x480    480p 1065k , avc1.4d401f, 30fps, video only, 24.99MiB
247          webm       1280x720   720p 1515k , vp9, 30fps, video only, 53.82MiB
136          mp4        1280x720   720p 2644k , avc1.4d401f, 30fps, video only, 65.17MiB
248          webm       1920x1080  1080p 2670k , vp9, 30fps, video only, 94.91MiB
137          mp4        1920x1080  1080p 4347k , avc1.640028, 30fps, video only, 157.74MiB
271          webm       2560x1440  1440p 9261k , vp9, 30fps, video only, 324.80MiB
313          webm       3840x2160  2160p 18654k , vp9, 30fps, video only, 656.19MiB
17           3gp        176x144    small , mp4v.20.3, mp4a.40.2@ 24k
36           3gp        320x180    small , mp4v.20.3, mp4a.40.2
43           webm       640x360    medium , vp8.0, vorbis@128k
18           mp4        640x360    medium , avc1.42001E, mp4a.40.2@ 96k
22           mp4        1280x720   hd720 , avc1.64001F, mp4a.40.2@192k (best)
```

# [Traffic Camera: Unwarp image](TrafficCamera_Unwarp_Image/README.md)

[![TrafficCamera_Unwarp_Image](TrafficCamera_Unwarp_Image/images/traffic.gif)](TrafficCamera_Unwarp_Image/README.md)

# [Traffic Camera: Darknet YOLOv3](TrafficCamera_Darknet_YOLOv3/README.md)

[![TrafficCamera_Unwarp_Image](TrafficCamera_Darknet_YOLOv3/images/yolov3.gif)](TrafficCamera_Darknet_YOLOv3/README.md)
