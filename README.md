# pro_23_playing_card_ml

## dependencies:
python >=3.8

### for direct installation
pip install ultralytics

## Training ML model:
model_train_pipeline.py
file contains a python script which accepts the args as pipeline script path, model to use for training, epochs, dataset path, batch size for training and name of model after training.

sample command:
python model_train_pipeline.py --model yolov8n.pt --num_epochs 50 --data C:/Users/vgvis/Downloads/data.yaml --batch 16 --name yolov8n_custom3

## dataset:
The model used for retraining are yolo provided bt ultralytics.So, the dataset should follow yolo guidlines.
To create custom dataset ::
https://github.com/ultralytics/yolov5/wiki/Train-Custom-Data

dataset should contain images and labels folder for training and validation purpose. This path sould be mentioned in the data.yaml file.

## Post-training::
the trained model on a custom dataset will be saved in new folder named runs.

## prediction:
prediction_pipeline.py
file contains a python script to predict results via trained ML model.The args to be passed are pipeline file path, model to used for prediction, the image or video file on which prediction to be done.

sample command:
python predict_pipeline.py --model B:/github_all_projects/pro23_playing_card_ml/card_predict(model1).onnx --source B:/github_all_projects/pro23_playing_card_ml/predict_image1.jpg

## Prediction using javascript code:
prediction.sh
Contains a javascript code which integrates python code with javascript.The above mentioned command can be passed via "pythonCommand" variable in the 'prediction.js' script 

the same process can be done where python command is saved in a shell script and this file is passed to javascript file named 'prediction_shell.js'


