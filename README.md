[//]: # "Image References"
[image1]: ./images/sample_dog_output.png "Sample Output"
[image2]: ./images/vgg16_model.png "VGG-16 Model Keras Layers"
[image3]: ./images/vgg16_model_draw.png "VGG16 Model Figure"

# Dog Breed Classifier

This repository has an accompanying [Medium Article](https://jbm1991.medium.com/identifying-dog-breeds-using-cnns-3ce770dbb57b)

## Project Overview

Welcome to the Convolutional Neural Networks (CNN) project in the AI Nanodegree! In this project, you will learn how to build a pipeline that can be used within a web or mobile app to process real-world, user-supplied images. Given an image of a dog, your algorithm will identify an estimate of the canine’s breed. If supplied an image of a human, the code will identify the resembling dog breed.

![Sample Output][image1]

Along with exploring state-of-the-art CNN models for classification, you will make important design decisions about the user experience for your app. Our goal is that by completing this lab, you understand the challenges involved in piecing together a series of models designed to perform various tasks in a data processing pipeline. Each model has its strengths and weaknesses, and engineering a real-world application often involves solving many problems without a perfect answer. Your imperfect solution will nonetheless create a fun user experience!

## Project Instructions

### Instructions

1. Clone the repository and navigate to the downloaded folder.

```sh
git clone https://github.com/udacity/dog-project.git
cd dog-project
```

1. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip). Unzip the folder and place it in the repo, at location `path/to/dog-project/dogImages`.

1. Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip). Unzip the folder and place it in the repo, at location `path/to/dog-project/lfw`. If you are using a Windows machine, you are encouraged to use [7zip](http://www.7-zip.org/) to extract the folder.

1. Donwload the [VGG-16 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG16Data.npz) for the dog dataset. Place it in the repo, at location `path/to/dog-project/bottleneck_features`.

1. (Optional) **If you plan to install TensorFlow with GPU support on your local machine**, follow [the guide](https://www.tensorflow.org/install/) to install the necessary NVIDIA software on your system. If you are using an EC2 GPU instance, you can skip this step.

1. (Optional) **If you are running the project on your local machine (and not using AWS)**, create (and activate) a new environment.

   - **Linux** (to install with **GPU support**, change `requirements/dog-linux.yml` to `requirements/dog-linux-gpu.yml`):

   ```sh
   conda env create -f requirements/dog-linux.yml
   source activate dog-project
   ```

   - **Mac** (to install with **GPU support**, change `requirements/dog-mac.yml` to `requirements/dog-mac-gpu.yml`):

   ```sh
   conda env create -f requirements/dog-mac.yml
   source activate dog-project
   ```

   **NOTE:** Some Mac users may need to install a different version of OpenCV

   ```sh
   conda install --channel https://conda.anaconda.org/menpo opencv3
   ```

   - **Windows** (to install with **GPU support**, change `requirements/dog-windows.yml` to `requirements/dog-windows-gpu.yml`):

   ```sh
   conda env create -f requirements/dog-windows.yml
   activate dog-project
   ```

1. (Optional) **If you are running the project on your local machine (and not using AWS)** and Step 6 throws errors, try this **alternative** step to create your environment.

   - **Linux** or **Mac** (to install with **GPU support**, change `requirements/requirements.txt` to `requirements/requirements-gpu.txt`):

   ```sh
   conda create --name dog-project python=3.5
   source activate dog-project
   pip install -r requirements/requirements.txt
   ```

   **NOTE:** Some Mac users may need to install a different version of OpenCV

   ```sh
   conda install --channel https://conda.anaconda.org/menpo opencv3
   ```

   - **Windows** (to install with **GPU support**, change `requirements/requirements.txt` to `requirements/requirements-gpu.txt`):

   ```sh
   conda create --name dog-project python=3.5
   activate dog-project
   pip install -r requirements/requirements.txt
   ```

1. (Optional) **If you are using AWS**, install Tensorflow.

```sh
sudo python3 -m pip install -r requirements/requirements-gpu.txt
```

1. Switch [Keras backend](https://keras.io/backend/) to TensorFlow.

   - **Linux** or **Mac**:

     ```sh
     KERAS_BACKEND=tensorflow python -c "from keras import backend"
     ```

   - **Windows**:

     ```sh
     set KERAS_BACKEND=tensorflow
     python -c "from keras import backend"
     ```

1. (Optional) **If you are running the project on your local machine (and not using AWS)**, create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `dog-project` environment.

```sh
python -m ipykernel install --user --name dog-project --display-name "dog-project"
```

1. Open the notebook.

```sh
jupyter notebook dog_app.ipynb
```

1. (Optional) **If you are running the project on your local machine (and not using AWS)**, before running code, change the kernel to match the dog-project environment by using the drop-down menu (**Kernel > Change kernel > dog-project**). Then, follow the instructions in the notebook.

**NOTE:** While some code has already been implemented to get you started, you will need to implement additional functionality to successfully answer all of the questions included in the notebook. **Unless requested, do not modify code that has already been included.**

## Evaluation

Your project will be reviewed by a Udacity reviewer against the CNN project [rubric](https://review.udacity.com/#!/rubrics/810/view). Review this rubric thoroughly, and self-evaluate your project before submission. All criteria found in the rubric must meet specifications for you to pass.

## Project Submission

When you are ready to submit your project, collect the following files and compress them into a single archive for upload:

- The `dog_app.ipynb` file with fully functional code, all code cells executed and displaying output, and all questions answered.
- An HTML or PDF export of the project notebook with the name `report.html` or `report.pdf`.
- Any additional images used for the project that were not supplied to you for the project. **Please do not include the project data sets in the `dogImages/` or `lfw/` folders. Likewise, please do not include the `bottleneck_features/` folder.**

Alternatively, your submission could consist of the GitHub link to your repository.
