# Training_Custom_SSD

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
  - Open new command propt, and cd into TF2_ObjDetect_API/models/research/ directory and run the following command:
    - # From within TensorFlow/models/research/
    - protoc object_detection/protos/*.proto --python_out=.
