# MA416_CIFAKE_Project
Riya Bharamaraddi, Ryan Bowering, Kayla Martinez, Adithya Ramji

## Introduction
AI image generation has been exploding in popularity over the past year, and it has become increasingly difficult to distinguish AI-generated images from real ones. Our goals were to train models to identify AI-Generated images, and find subtle differences between AI-generated and real images that could be further explored to make distinguishing them easier. We used the [CIFAKE](https://www.kaggle.com/datasets/birdy654/cifake-real-and-ai-generated-synthetic-images) Dataset containing 120,000 images for this project.

This is a continuation of a project from MA415 last spring. Check out that repo: https://github.com/rhit-bowerirn/MA415_AI_Real_Images

## Human Baseline test
Want to see how well you can identify AI-generated images from the CIFAKE dataset? Take our [human baseline](https://docs.google.com/forms/d/e/1FAIpQLSfF5GdTvXe9jbBRdy-UBmN0t7ICy4631gzULimW0ParjxaxZg/viewform) test! It contains 15 randomly selected images from the dataset for you to try classifying.

## Instructions

### Running the notebooks
Most of these notebooks are set up to be run in Google Colabs out of the box, though they can be run on any Jupyter server if you install the necessary packages. On Colabs, you will need to add the data files to the runtime. Accessing the data on other servers may vary depending on how you set up your directory.

There are two notebooks that should be run on Kaggle: `kaggle-data-compression.ipynb` and `ViT.ipynb`. Add the `CIFAKE: Real and AI-Generated Synthetic Images` dataset to the environment and the notebooks should run.

### Getting the data
1. Open the `kaggle-data-compression.ipynb` notebook in Kaggle, and add the CIFAKE dataset. Run the notebook and download the `CIFAKE_Train.npz` and `CIFAKE_Test.npz` files (further instructions in the notebook)
2. Using those data files, run the notebooks in the `filters` directory and download the `.npz` files.

### Running models
Once you have all the data files, just open a notebook from the models folder and add the data to the runtime environment for Colabs (or add them to your server of choice), and you should be set to run the models. 

The `ViT.ipynb` will need to be imported to Kaggle with the CIFAKE dataset added to the environment and GPU enabled. It will run fastest on the T4 (x2) GPUs since it limits its batch size per device for those. If you want to use the P100, you can double the per-device batch size in the `TrainerArguments` object
