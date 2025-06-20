
# Image Captioning with Speech Synthesis 

An end-to-end deep learning pipeline that takes an input image, generates a descriptive caption, and converts that caption into human-like speech using integrated Text-to-Speech (TTS) synthesis.


## Project Highlights

**CNN + RNN Architecture**: Uses DenseNet for feature extraction and GRU for caption generation.
**Integrated Speech Synthesis**: Converts text to speech using `gTTS` or `pyttsx3`.
**Dataset**: Trained and evaluated on the **Flickr8k** dataset.
**End-to-End Pipeline**: From image → caption → audio.

## Model Architecture

###  1. CNN for Feature Extraction
**Model**: Pretrained **DenseNet201** from Keras (trained on ImageNet).
**Purpose**: Extract high-level features from images.
**Preprocessing**:
   Resize images to a fixed shape.
   Normalize pixel values.

### 2. RNN for Caption Generation
**Model**: GRU (Gated Recurrent Unit)
**Components**:
   Word Embeddings
   GRU-based sequence decoder
   Dense output layer
   
**Loss Function**: Categorical Crossentropy
**Optimizer**: Adam

## Dataset

**Flickr8k Dataset**
   8,091 images
   5 captions per image
**Format**:
   Captions stored in a text file: `image_name.jpg\tCaption text`
   Images and captions are preprocessed and tokenized


## 🔊 Text-to-Speech Module

Converts the generated caption into speech
Two options:
  [`gTTS`](https://pypi.org/project/gTTS/) (Google Text-to-Speech – cloud-based)
  [`pyttsx3`](https://pypi.org/project/pyttsx3/) (offline engine)
