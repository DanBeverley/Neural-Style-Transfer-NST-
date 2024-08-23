# Neural Style Transfer

This repository contains an implementation of **Neural Style Transfer (NST)** using TensorFlow. NST is a fascinating application of deep learning where the content of one image is combined with the style of another to generate a visually appealing piece of art.

## How It Works

Neural Style Transfer is performed using a Convolutional Neural Network (CNN). The core idea is to take two images: a **content image** and a **style image**. The content image provides the structure or layout, while the style image provides the texture and color scheme. The process involves:

1. **Extracting Features**: We use a pre-trained CNN (e.g., VGG19) to extract feature maps from different layers of the network. The deeper layers capture the content of the image, while the shallower layers capture the style.

2. **Defining Loss Functions**:
    - **Content Loss**: Measures how different the content of the generated image is from the content image.
    - **Style Loss**: Measures how different the style of the generated image is from the style image.
    - **Total Variation Loss**: An optional regularization term that helps smooth the generated image.

3. **Optimization**: We use gradient descent to minimize the combined loss (content + style + total variation), updating the pixels of the generated image until it closely resembles the desired output.

## Usage

1. **Follow the Notebook**: The notebook is structured to guide you through the entire process of Neural Style Transfer, from loading images to generating the final output. Each code cell has accompanying explanations.

2. **Run the Code**: You can run the cells one by one to understand how each component works, or you can run all cells to see the full process in action.


## Customization

You can customize the following aspects of the Neural Style Transfer:

- **Images**: Replace the content and style images in the `images/content/` and `images/style/` directories with your own.
- **Hyperparameters**: Adjust the weights for content, style, and total variation loss in the notebook to see how it affects the output.
- **Model**: Experiment with different pre-trained models like VGG16 or even deeper networks.

## Troubleshooting

If you encounter any issues, consider the following:

- **Memory Issues**: NST can be memory-intensive, especially with large images. Consider resizing images or using a machine with a GPU.
- **Blurry Output**: If the generated image is too blurry, try increasing the weight of the content loss or reducing the number of iterations.
- **Installation Problems**: Ensure all dependencies are correctly installed by running `pip install -r requirements.txt`.
