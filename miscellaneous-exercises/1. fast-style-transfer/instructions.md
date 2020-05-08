## Instructions

1. Install miniconda or anaconda if you have not already.
2. Open command prompt and enter these commands line by line:
    `conda create -n style-transfer python=3`
   ` conda activate style-transfer`
   ` conda install tensorflow scipy pillow`
   ` pip install moviepy`
   ` python -c "import imageio; imageio.plugins.ffmpeg.download()"`
   
   ***Note:*** *If you get an error on the last command that ends in*
   `'RuntimeError: imageio.ffmpeg.download() has been deprecated. Use 'pip install imageio-ffmpeg' instead.' `
    *just run the command `pip install imageio-ffmpeg`. You may need to restart the terminal and reactivate the environment for the command to complete.*

3. Download the Zip archive from the [fast-style-transfer repository](https://github.com/lengstrom/fast-style-transfer) and extract it. You can download it by clicking on the bright green button on the right.
4. Download the Rain Princess checkpoint from [here](https://d17h27t6h515a5.cloudfront.net/topher/2017/January/587d1865_rain-princess/rain-princess.ckpt). Put it in the fast-style-transfer folder. A checkpoint file is a model that already has tuned parameters. By using this checkpoint file, we won't need to train the model and can get straight to applying it.
5. Copy the image you want to style into the fast-style-transfer folder.
6. Enter the Conda environment you created above, if you aren't still in it.
7. Finally, in your terminal, navigate to the fast-style-transfer folder and enter
    `python evaluate.py --checkpoint ./rain-princess.ckpt --in-path <path_to_input_file> --out-path ./output_image.jpg`
    ***Note:***  *Your checkpoint file might be named rain_princess.ckpt, notice the underscore, it's not the dash from above.*
