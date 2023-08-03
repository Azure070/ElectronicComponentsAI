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

View a video explanation here: 
