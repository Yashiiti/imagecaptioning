# imagecaptioning
## Usage:
Open the notebook to see the entire code about building an image captioning model from scratch. This model takes as input images and captions associated with them it learns by converting the image into image features which are accomplished by a pre-trained model here, then it works similarly to an encoder decoder-based machine translation model instead of translating a language it translates the image features into captions. The decoder is based on transformers.
The Notebook is quite big so might not load use the collab link:https://colab.research.google.com/drive/1N-VmP6_0XGsbMKU99uFIOTZ7LP_NMvvm?usp=sharing
## Training an image captioning model from scratch
If you wish to train the Image Captioning model from scratch, follow these additional steps:

Prepare the dataset: Gather a dataset of images paired with their corresponding captions. Ensure that each image is associated with one or more captions to form training pairs.

Preprocess the data: Transform the images into a suitable format for training the model. Extract visual features using techniques such as pre-trained convolutional neural networks (CNNs) like ResNet or InceptionV3 or MobileNetV3.

Tokenize the captions: Convert the textual captions into token sequences that can be fed into the transformer model. Apply techniques like word-level or subword-level tokenization.

Define the model architecture: Construct the transformer-based model architecture for the image captioning task. This typically involves combining a CNN encoder with a transformer decoder. I used a pre-trained MobileNetV3 as a pre-trained CNN.

Train the model: Train the model using the preprocessed dataset. This usually involves optimizing a loss function such as cross-entropy between the predicted captions and the ground truth captions. I used sparse categorical cross entropy with logits which calculates loss between actual and predicted probabilty distribution of labels.

Save the model weights: Save the trained model's weights as a checkpoint file for later usage or fine-tuning.
