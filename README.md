# Traffic-Sign
Import Libraries:

It uses OpenCV to read and resize images, NumPy to handle arrays, and TensorFlow/Keras to load and use the trained model.

Load the Trained Model:

A model that was already trained to recognize traffic signs is loaded from a .h5 file. This file contains everything needed to make predictions — the model architecture and its learned weights.

Prepare the Input Image:

A test image (e.g. a photo of a traffic sign) is loaded. The image is resized to match the input size expected by the model (typically 32×32 pixels), and the pixel values are scaled from 0–255 down to a 0–1 range for better performance. Finally, the image is reshaped so the model sees it as a batch (even though it's just one image).

Make a Prediction:

The image is passed through the model, which outputs a list of probabilities — one for each possible class (e.g., speed limit signs, stop signs, etc.).

Determine the Predicted Class:

The class with the highest probability is chosen as the model's prediction. This is returned as a number (e.g. 0, 14, 33), which corresponds to a specific traffic sign.

Print the Result:

The predicted class ID is printed. If you have a mapping of IDs to traffic sign names (like 0 = "Speed Limit 20", 1 = "Stop", etc.), you can use it to display the actual sign name.

