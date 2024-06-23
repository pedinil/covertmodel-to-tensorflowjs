
# Importing Keras Model in Google Colab and Converting to TensorFlow.js

This repository contains the steps to import a Keras model in Google Colab and convert it to TensorFlow.js for deployment on the web.

### Steps:

1. Import the Keras model to Google Colab:
   - Upload the saved Keras model file (.h5) to your Google Drive or import it by python
   - Mount your Google Drive in Colab and load the model using Keras' `load_model` function.

2. Convert the Keras model to TensorFlow.js format:
   - Install the TensorFlowjs in python package using pip:
     ```
     !pip3 install tensorflowjs
     ```
   - Convert the Keras model to TensorFlow.js format using the following command:
     ```
     !tensorflowjs_converter --input_format keras /tmp/mobilenetv2/save_model.h5 /tmp/mobilenetv2/
     ```

3. Load and use the TensorFlow.js model in your web application:
   - Include the TensorFlow.js script in your HTML file:
     ```html
     <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs"></script>
     ```
   - Load the converted TensorFlow.js model using `tf.loadLayersModel`.
   - Use the loaded model for inference in your web application.



