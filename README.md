# ElectronicComponentsAI

 This model identifies and classifies a few basic electronic components. This model might be helpful to sorting algorithims.

## The Algorithm

This model was created on Jetson Nano and trained on a dataset of electrolytic capacitors, integrated circuits, leds, potentiometers, resistors, semiconductor diodes, and transistors. It uses an imagenet.py program to classify each component


## Running this project

1. Have the Jetson Inference library and python3 both installed on your Jetson Nano.
2. Download the model_best.pth.tar from https://drive.google.com/drive/folders/1xtHEz4bTSl7l_4BDBZU-SeldpwhSp84e 
3. Open docker container from jetson-inference directory
```
./docker/run.sh
```
4. Setup resNet in the jetson-inference/python/training/classification directory with this command
```
python3 onnx_export.py --model-dir=models/ElectronicsAI
```
5. Exit the docker container
6. Set the net and dataset arguments with these commands below
```
   NET=models/ElectronicAI
   DATASET=models/ElectronicAI
```
7. Run this command to see how this works from
```
imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/electrolyticCapacitor/eCapacitor0.jpg eCapacitor.jpg
```


View a video explanation here: 
