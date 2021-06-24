# Install Tensorflow Object Detection API

Download and install Visuall Studio and check Desktop Development with C++.

Download and install Git.

### Install necessary library.

Open Command Propt with Administrator with python > 3.5 (I used version 3.7) and tensorflow=2.4.1

        pip install -r requirements.txt
COCO
 
        pip install git+https://github.com/philferriere/cocoapi.git#subdirectory=PythonAPI

## A. You install and setup Tensorflow Object Detection API.

with [Object Detection API with TensorFlow 2](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2.md)

- ### 0. Create TF2_ObjDetect_API folder and open command propt in here ![image](https://user-images.githubusercontent.com/76576719/119085857-b7368e80-ba2e-11eb-9daf-127977fe78bf.png)

- ### 1. Download models of tensorflow api with: 
    
        git clone https://github.com/tensorflow/models.git

in Tensorflow folder and `cd models`.

- ### 2. You set variable `PYTHONPATH` in System variables.

- ![image](https://user-images.githubusercontent.com/76576719/119085684-5f982300-ba2e-11eb-8567-713d264814f0.png)

- ### 3. Protobuf Installation and Compilation.

  - Head to the [protoc releases page](https://github.com/protocolbuffers/protobuf/releases)
  
  - Download last release (e.g protoc-3.17.0-win64.zip) in the TF2_ObjDetect_API Folder.
  
  - Extract file here in the TF2_ObjDetect_API Folder and then rename Google Protobuf ![image](https://user-images.githubusercontent.com/76576719/119086064-1eecd980-ba2f-11eb-9be7-7dc318c8b5d4.png)
 
  - Add path directory Google Protobuf to your `Path` environment variable.
    
    note:   The path will be set temporarily, to make the change permanent you have to set it in the “Advanced system settings” → “Environment Variables” tab. 
            Restart The Cmd or PowerShell window for changes to take effect.
  
  - ![image](https://user-images.githubusercontent.com/76576719/122653765-20fea100-d171-11eb-87a9-f50026647491.png)

  - Open new command propt, and cd into TF2_ObjDetect_API/models/research/ directory and run the following command:
  
        protoc object_detection/protos/*.proto --python_out=.`

- ### 4. Build and install.
  We choose one of two ways.
  Copy TF2_ObjDetect_API\models\research\object_detection\packages\tf2\setup.py into TF2_ObjDetect_API\models\research
  - 4.1 run the following command from within TF2_ObjDetect_API\models\research:
               
        python setup.py built
    
        python setup.py install
                
  - 4.2 run the following command from within TF2_ObjDetect_API\models\research: 
   
        python -m pip install .
  
- ### 5. Test your Installation.

  - run the following command from within TF2_ObjDetect_API\models\research: 
  
        python object_detection/builders/model_builder_tf2_test.py
  
  - If the result is as shown in the image below, then you are successful.
 
  - ![image](https://user-images.githubusercontent.com/76576719/122653738-e7c63100-d170-11eb-944a-65b9758aceab.png)

