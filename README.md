# Protobuf-Dreamer
A tiled DeepDream project for creating any size of image, on both CPU and GPU


### Dependencies: 

`sudo apt-get install python-skimage`

`sudo pip install python-pip`

`sudo pip install numpy`

`sudo pip install scipy`

`sudo pip install tensorflow`

### Setup:

Run the following to download and setup the default model:

`cd Protobuf-Dreamer` 

`wget https://storage.googleapis.com/download.tensorflow.org/models/inception5h.zip`

`unzip -d model inception5h.zip`

### Usage: 

Basic usage: 

```
python pb_dreamer.py --input_image input.png
```

Advanced usage: 

```
python pb_dreamer.py --input_image input.png --output_image output.png --octaves 4 --layer mixed4d_3x3_bottleneck_pre_relu --channel 139 --iter 10 --tile_size 512 --model /home/ubuntu/DeepDream/model/tensorflow_inception_graph.pb
```

### Parameters: 

* `--input_image`: The input image for performing DeepDream on. Ex: `input.png`

* `--output_image`: The name of your output image. Ex: `output.png`

* `--layer`: The target layer. Ex: `mixed4d_3x3_bottleneck_pre_relu`.

* `--channel`: The desired channel of the target layer. Ex: `139`.

* `--tile_size`: The desired size of tiles to use. Ex: `512`.

* `--iter`: The number of iterations. Ex: `10`.

* `--Octaves`: The number of octaves. Ex: `4`.

* `--model`: Path to the `.pb` model file. Default is `tensorflow_inception_graph.pb`.
