## Overview:
- This web app uses object recognition to identify a hand-drawn electrical circuit diagram and reconstruct it in a digital format (LTspice schematic). It then displays simulation results on the circuit in the form of voltages and currents.

![general overview v2](https://github.com/dl423/web-app-for-circuit-analysis/assets/81783344/c2ec7baf-dc44-49bd-80b3-b90129d23620)

## 30-Second Video Demo:

https://github.com/dl423/web-app-for-circuit-analysis/assets/81783344/f44be5da-9fe3-43c5-87f9-a9acbafa9c42


## Technical implementation:
- Programming language: Python
- Programming platform: Google Colab
  - The back-end of the program comprises of two Colab notebooks. One notebook is run in hosted runtime and is responsible for executing most of the functionalities. The other notebook is run locally on a computer to communicate with LTspice.
- Front-end of the web app is implemented using Anvil
- Used YOLOv5 object recognition model to identity the circuit elements (resistors, voltage sources, etc.) and the numerical values
  - Dataset images were annotated using Roboflow
  - Training of the model was done on a Colab notebook template provided by YOLOv5's github page 
- EasyOCR is used to recognize the value of numbers
- Hough Line Transform in OpenCV library was used to detect the wires
  - This algorithm detect straight line segments in the image
- The program communicated with LTspice to run circuit simulation and retreive simulation results 
______


![media-2](https://github.com/dl423/web-app-for-circuit-analysis/assets/81783344/b725bcbe-a572-4226-82d3-b35bd4780279)

![media-3](https://github.com/dl423/web-app-for-circuit-analysis/assets/81783344/dcdc07c4-6264-4d75-8f72-762651ca5e62)

