# Install Tensorflow Object Detection API

### Install necessary library
- Open Command Propt with Administrator with python > 3.5
- pip install numpy
- pip install pillow
- pip install lxml
- pip install matplotlib
- pip install jupyter
- pip install tensorflow==2.4.1
- pip install tensorflow-gpu==2.4.1 (if cuda 11.0 for GPU)
- # COCO API
- pip install cython
- pip install git+https://github.com/philferriere/cocoapi.git#subdirectory=PythonAPI

## A: You install and setup Tensorflow Object Detection API 
with [Object Detection API with TensorFlow 2](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2.md) or [Tensorflow 2 Object Detection tutorial](https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/install.html#tensorflow-object-detection-api-installation)

- ### 0. Create TF2_ObjDetect_API folder and open command propt in here ![image](https://user-images.githubusercontent.com/76576719/119085857-b7368e80-ba2e-11eb-9daf-127977fe78bf.png)

- ### 1. Download models of tensorflow api with: `git clone https://github.com/tensorflow/models.git` in Tensorflow folder and `cd models`

- ### 2. You set variable `PYTHONPATH` in System variables

- ![image](https://user-images.githubusercontent.com/76576719/119085684-5f982300-ba2e-11eb-8567-713d264814f0.png)

- ### 3. Protobuf Installation and Compilation

  - Head to the [protoc releases page](https://github.com/protocolbuffers/protobuf/releases)
  - Download last release (e.g protoc-3.17.0-win64.zip) in the TF2_ObjDetect_API Folder
  - Extract file here in the TF2_ObjDetect_API Folder and then rename Google Protobuf ![image](https://user-images.githubusercontent.com/76576719/119086064-1eecd980-ba2f-11eb-9be7-7dc318c8b5d4.png)
  - Add path directory Google Protobuf to your `Path` environment variable
  - ![image](https://user-images.githubusercontent.com/76576719/119086595-e7caf800-ba2f-11eb-96ea-b258a34b3339.png)
  - Open new command propt, and cd into TF2_ObjDetect_API/models/research/ directory and run the following command:
    - `protoc object_detection/protos/*.proto --python_out=.`
- ### 4. Build and install
  We choose one of two ways
  - 4.1 Copy TF2_ObjDetect_API\models\research\object_detection\packages\tf2\setup.py into TF2_ObjDetect_API\models\research
  - run the following command from within TF2_ObjDetect_API\models\research:
    - python setup.py built
    - python setup.py install
  - 4.2 run the following command from within TF2_ObjDetect_API\models\research: `python -m pip install .`
- ### 5. Test your Installation
  - run the following command from within TF2_ObjDetect_API\models\research: 
  - `python object_detection/builders/model_builder_tf2_test.py`
  - If the result is as shown in the image below, then you are successful 
  - ![image](![image](https://user-images.githubusercontent.com/76576719/121954132-9856be00-cd88-11eb-835e-ab68d410a406.png)
