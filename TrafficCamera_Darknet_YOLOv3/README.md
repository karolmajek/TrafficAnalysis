# Darknet YOLOv3

![YOLOv3](images/yolov3.gif)

Here is the [Darknet YOLOv3 page](https://pjreddie.com/darknet/yolo/)

Dakrnet is submodule of this repository, you can find sources in `darknet` directory.

# Building with GPU

If you don't want to use GPU you can skip next step.

If you don't want to use webcam input you can compile without OpenCV.

## Enable GPU, CUDNN, and OpenCV

We will need to modify `Makefile`. By default it doesn't support GPU, CUDNN, and OpenCV.

```
GPU=1
CUDNN=1
OPENCV=1
OPENMP=0
DEBUG=0
```

On Linux you can modify it usind `sed`. Of course you can use your favorite text editor...

```
sed -i -e 's/GPU=0/GPU=1/g' darknet/Makefile
sed -i -e 's/CUDNN=0/CUDNN=1/g' darknet/Makefile
sed -i -e 's/OPENCV=0/OPENCV=1/g' darknet/Makefile
```

## Building

We are ready to build, we will go to the `darknet` directory and build:

```
cd darknet
make -j 8
```

# Download weights

We will download weights from Darknet YOLO website:

```
wget https://pjreddie.com/media/files/yolov3.weights
```

# Run Webcam Demo!

If you compiled darknet with OpenCV you can run a webcam demo. You can change detection threshold with `-thresh` option

```
./darknet detector demo cfg/coco.data cfg/yolov3.cfg yolov3.weights -thresh 0.5
```

# Run on video

You can download the video with youtube-dl:

```
youtube-dl -f 313 MNn9qKG2UFI
```

Since names.list is required by darknet to work, we will create a link to MS COCO names:

```
cd data m
ln -s coco.names names.list
cd ..
```

Finally, we can run detections on the video!

```
./darknet detector demo cfg/yolov3.cfg cfg/yolov3.cfg yolov3.weights   -thresh 0.5 -prefix results/yolov3-traffic-camera
```

Results will be written to `results` directory in separate files named `yolov3-traffic-camera_%08d.jpg` where `%08d` is the index with leading zeros.

## Create .gif

You can use ImageMagick `convert`. We will use only 100 frames 200-299:

```
convert -resize 320x240 -delay 2 -loop 0 results/*000002*.jpg yolov3.gif
```

![YOLOv3](images/yolov3.gif)

## Create .mp4

Finally, we will create a mp4 video from all frames using `ffmpeg`. If H265 doesn't work on your PC you can use H264 by replacing `libx265` with `libx264`:

```
ffmpeg -pattern_type glob -i 'results/*.jpg' -c:v libx265 yolov3.mp4
```
