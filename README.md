# **Real-Time Traffic Sign Recognition with OAK-D** #

## Introduction

<h4><strong>This project was created in 2023 as part of a university course on Computer Vision. It utilizes Python 3.10.12 and focuses on existing image processing techniques.

The project expands upon [canozcivelek's traffic-sign-recognition](https://github.com/canozcivelek/traffic-sign-recognition), integrating recent advancements. </h4></strong>

![Cildren crossing](Images/OAK-D Camera_screenshot_29.03.2024.png)

## Highlights

- **Updated Libraries:** I've updated nearly all dependencies to their latest stable versions to ensure the project runs smoothly on Python 3.10.12, benefiting from enhanced features and security.

- **Live OAK-D Camera Integration:** A new feature allows live testing of the trained model with the OAK-D camera, paving the way for real-world application and evaluation.

## Getting Started

**Clone the Repository**

To get started, clone this repository using HTTPS:
```bash
git clone https://github.com/svndin/image-processing-lab
```
**Set Up Your Environment**

Navigate to the project directory and create a virtual environment:
```bash
cd image-processing-lab
python3 -m venv image-processing
source image-processing/bin/activate
```
**Install the Dependencies:**

Install the necessary Python packages from the [requirements.txt](https://github.com/svndin/image-processing-lab/blob/main/requirements.txt) file:
```bash
python3 -m pip install -r requirements.txt
```

## Running the Project

**Launch Jupyter Notebook**

Within the project directory, start Jupyter Notebook:
```bash
jupyter notebook
```
Navigate through the interface to open the provided [New_trafficSigns.ipynb](https://github.com/svndin/image-processing-lab/blob/main/New_trafficSigns.ipynb) notebook.

**Explore the Notebooks**

1. **New_trafficSigns.ipynb:** Start here to understand the project structure and logic.
2. **Sequential Execution:** Follow the notebook, executing code blocks in order to train your model.
3. **Model Creation:** Step-by-step instructions will guide you through creating and saving your traffic sign recognition model.

**Final Notes**

- After training, compare your model's predictions (Predicted sign: [ ]) with the correct signs listed in [signnames.csv](https://github.com/svndin/image-processing-lab/blob/main/signnames.csv).
- For a detailed guide on setting up the OAK-D camera, refer to the instructions in the next section.

 

#
# **Running the model using the OAK-D**

The [New_OAK-D.ipynb](https://github.com/svndin/image-processing-lab/blob/main/New_Oak-D.ipynb) notebook takes the project to the next level by integrating live traffic sign recognition using the OAK-D camera. This section allows you to apply the traffic sign recognition model in real-world scenarios, showcasing the practical application of the technology.   

**OAK-D Camera Setup**

To use the OAK-D camera for live recognition, use this command for Linux users. (Users of other operating systems should consult the  [Luxonis documentation](https://docs.luxonis.com/en/latest/pages/tutorials/first_steps/).)
```bash
sudo wget -qO- https://docs.luxonis.com/install_depthai.sh | bash
```

## Setup and Use

1. **Model Preparation:** The project utilizes the model created in [New_trafficSigns.ipynb](https://github.com/svndin/image-processing-lab/blob/main/New_trafficSigns.ipynb). For ease of use, a pre-trained model,  [new_traffic_signs_model.keras](https://github.com/svndin/image-processing-lab/new_traffic_signs_model.keras), is also provided in the repository.

2. **Notebook Execution:** Open and run the [New_OAK-D.ipynb](https://github.com/svndin/image-processing-lab/blob/main/New_Oak-D.ipynb) notebook within the Jupyter Notebook environment. This notebook guides you through the process of running the live recognition system using the OAK-D camera.

3. **Live Recognition:** As you proceed with the notebook, you'll be able to perform live traffic sign recognition. The system uses the camera feed to detect signs and display their classifications in real-time.
#

## Enhancing the Model with OpenVINO and blobconverter
Maximize your OAK-D camera's capabilities by incorporating depth functionality with OpenVINO and blobconverter. This process not only enhances model accuracy but also enables depth sensing for superior performance.

**Optimizing with OpenVINO**

First, install OpenVINO to optimize your model for Intel hardware, which significantly boosts performance. Detailed installation instructions are available on OpenVINO's official documentation page: [OpenVINO](https://docs.openvino.ai/latest/openvino_docs_install_guides_installing_openvino_linux.html).

**Converting with blobconverter**

Next, convert your optimized model to a blob format using blobconverter, ensuring compatibility with the OAK-D. This conversion can be done easily at [blobconverter.luxonis](https://blobconverter.luxonis.com).

**Deploy and Recognize with Depth**

Finally, deploy the optimized and converted model on your OAK-D camera. This upgrade not only enhances traffic sign recognition but also provides insights into their spatial positioning, adding a new dimension of depth and accuracy to your system.

#

Let's continue to explore, innovate, and transform the world, one traffic sign at a time. Happy coding!
