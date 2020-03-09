# Edge_app_to_detect_pose_or_text_or_car
In this repository, a simple application of Edge computing is shown to detect human pose or text or car type/color from an image using Intel's OpenVINO Toolkit

### Introduction:
This task is an assignment of Udacity's Edge Computing with OpenVINO course. In this task we use 3 prebuilt models to determine the image contains a car or pose or text.

The environment used is provided by Udacity, following executes the image across the model and gives output embedded on the image. The app.py file is in the repository and handle_models.py file is also in repository. app.py file makes use of handle_models to determine the contents of image.

For CAR we : 
python app.py -i "images/blue-car.jpg" -t "CAR_META" -m "/home/workspace/models/vehicle-attributes-recognition-barrier-0039.xml" -c "/opt/intel/openvino/deployment_tools/inference_engine/lib/intel64/libcpu_extension_sse4.so"

![car_image](https://user-images.githubusercontent.com/41015749/76257175-315e6700-621f-11ea-86a9-b7f47972c6e7.png)

For text, we use:

python app.py -i "images/sign.jpg" -t "TEXT" -m "/home/workspace/models/text-detection-0004.xml" -c "/opt/intel/openvino/deployment_tools/inference_engine/lib/intel64/libcpu_extension_sse4.so"

![text_estimation](https://user-images.githubusercontent.com/41015749/76257604-01639380-6220-11ea-9312-13338f74318b.png)

For pose estimation, we use:

python app.py -i "images/sitting-on-car.jpg" -t "POSE" -m "/home/workspace/models/human-pose-estimation-0001.xml" -c "/opt/intel/openvino/deployment_tools/inference_engine/lib/intel64/libcpu_extension_sse4.so"

![pose_estimation](https://user-images.githubusercontent.com/41015749/76257607-0294c080-6220-11ea-93a5-31370cf99bee.png)

### Conclusion:
This exercise, enabled me to design edge computing app to detect text,pose or car type using Intel's OpenVINO toolkit.
