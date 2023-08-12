# face_mask_detection
To detect the face mask of of the person using VGG16. 



![Face Mask Detection Demo](demo.gif)

## Objective

The objective of this project is to develop a real-time face mask detection system using deep learning techniques. The system aims to classify whether a person is wearing a face mask or not, contributing to safety measures during the ongoing pandemic.

## Approach

The project follows these key steps:

1. **Data Collection and Preprocessing**: The dataset consists of images of individuals with and without face masks. Images are resized to 224x224 pixels to match the input size of the VGG16 model.

2. **Transfer Learning with VGG16**: The VGG16 pre-trained model is utilized as a feature extractor. The last fully connected layer is replaced with a new dense layer for binary classification (with mask or without mask). Only the weights of the new layer are trained, keeping the VGG16 layers frozen.

3. **Model Compilation**: The model is compiled using the Adam optimizer, binary cross-entropy loss function, and accuracy as a metric.

4. **Real-Time Face Mask Detection**: OpenCV is employed to capture video from the webcam in real-time. Each frame is processed by the model to predict whether a face is wearing a mask. The prediction result is overlaid on the video stream.

## Results

- Achieved an accuracy of approximately 94% on the training data and 93% on the validation data.
- Real-time face mask detection demonstrated on moving people captured by the webcam.
- The model effectively labels individuals as "with mask" or "without mask" in the video stream.

## Usage

1. Clone the repository:


2. Install the required libraries (ensure you have Python and pip installed):


3. Run the main script:


4. Press the 'x' key to exit the real-time detection.

## Future Enhancements

- Improve model robustness and accuracy through hyperparameter tuning and data augmentation.
- Deploy the model on edge devices for real-world applications.
- Expand the project to detect face masks in images and videos stored locally.

## Credits

- Dataset: [https://pyimagesearch.com/2020/05/04/covid-19-face-mask-detector-with-opencv-keras-tensorflow-and-deep-learning/]

- Libraries: TensorFlow, Keras, OpenCV
