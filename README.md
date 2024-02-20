# Music Generation

This repository contains the code and resources for an Automatic Music Generation project. The project aims to generate original compositions using machine learning techniques.

Music Generation is a project focused on automatically generating music compositions. The project utilizes machine learning algorithms to generate original pieces of music based on classical compositions by famous musicians such as Schubert, Chopin, and Mozart.

The project is implemented using Python and various libraries and frameworks for machine learning and music processing. The generated music is primarily focused on classical instrumentation, particularly piano music.

This repository serves as a central hub for the project, providing access to the source code, documentation, and resources related to the music generation process.

## Table of Contents

- [Introduction](#introduction)
- [Requirements](#requirements)
- [Project Architecture and Approach](#project-architecture-and-approach)
- [Results](#results)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Usage](#usage)
- [Contribution Guidelines](#contribution-guidelines)
- [License](#license)
- [Acknowledgement](#acknowledgement)
- [Contact Information](#contact-information)

## Introduction

- Composition of music requires in-depth knowledge on the subject itself. With this project we hope to work towards simplifying the process so even people with lesser technical knowledge can create their own tunes.

- Automatic Music Generation is an application that will compose short pieces of piano music. It aims to generate notes and rhythms randomly every time. The sequence will then be converted into an MIDI file, a type audio file, which will be downloaded into the system.

- The project involves the use of Feed Forward Neural Network concepts, WaveNet in particular. The application will be composing short pieces of piano music.

- The model is created with WaveNet algorithms and several classical music pieces which serve as data for the model to train.

- The model generates a sequence of notes and beats. This sequence is converted into an MIDI file which is downloaded and can be played by the user.

## Requirements

To run the music generation code, you need the following requirements:

- Python 3.x
- TensorFlow
- NumPy
- MIDIUtil
- Music21

For detailed installation instructions, refer to the [Installation](#installation) section.

## Project Architecture and Approach


![Project Flow](https://github.com/YVandana/Music-Generation/assets/80910772/51844ea1-e8a2-4f82-9dbe-a93942fa0dfe)


The proposed architecture is using WaveNet, a convolution neural network (CNN) and is used to generate raw audio. It is a type of feedforward neural network. 

In WaveNet, the CNN takes a raw signal as an input and synthesis an output one sample at a time. It does so by sampling from a softmax distribution of a signal value that is encoded using µ-law compounding transformation and quantized to 256 possible values.
This project uses1-D convolution here. Hence, the reason why we chose to use this approach in our project due to the specialty of the method to deal with raw audio and also in our research and experimentation we found that this gives us clearer outputs.

The raw audio is provided through MIDI Data. For MIDI data to be read and later converted we use the music21 library.

The data is explored and a summary is taken. Then the data is prepared to be split into training and test data sets. This training data is given to the WaveNet algorithm which is implemented through the keras library and models are created from there the best model i.e. model with the most improved loss value is taken and then sequences are generated using the random function along with the predictions from the model.

The model is then converted to a MIDI file which can be downloaded and played.


## Results

Here are some screenshots of the Coding process:

Screenshot of the execution of Model Summary:

![Model Summary](https://github.com/YVandana/Music-Generation/assets/80910772/54ffb5fb-1ca0-4e9d-b815-e810ed001e25)

Screenshot of an Example Generated Sequence Which is to be Converted into a MP3 File:

![Example Generated Sequence](https://github.com/YVandana/Music-Generation/assets/80910772/170f9dec-964d-4285-b0c3-82d5fcad23b9)

Here is the Video to View the Output (Directs to YouTube):

[![Output](https://img.youtube.com/vi/03zDzlMZ2DA/0.jpg)](https://www.youtube.com/watch?v=03zDzlMZ2DA)


Example Outputs can be found in the Outputs Folder in the Repository.

## Repository Structure
- Code: This directory contains the implementation of the brain tumor detection and classification system. It includes script for data preprocessing, model generation and creating and downloading MP3 File.
- Datasets: This directory is used to store the labeled dataset of MIDI Files.
- Outout: This directory is used to store some MIDI and MP3 Outputs.
- LICENSE: This file contains the license information for the project.

## Getting Started
To get started with the project, follow these steps:
1. Clone the repository: git clone https://github.com/YVandana/Music-Generation.git
2. Explore the readme to understand the implementation details.
3. Run the scripts in the appropriate order to preprocess the data, train the CNN model, and generate MP3 Files.
4. Refer to the project report in the report/ directory for a comprehensive understanding of the project methodology and results.

## Installation

To get started with the project, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/YVandana/Music-Generation.git
   ```

2. Install the required dependencies. You can use `pip` to install the dependencies:

   ```bash
   pip install tensorflow numpy midiutil music21
   ```

3. Once the dependencies are installed, you are ready to use the code for music generation.

## Usage

To generate music using the provided code, follow these steps:

1. Navigate to the project directory:

   ```bash
   cd Music-Generation
   ```

2. Run the music generation script:

   ```bash
   python generate_music.py
   ```

   This script will use the trained machine learning model to generate a new composition.

3. The generated music will be saved as a MIDI file in the `output` directory.

Feel free to explore the code and experiment with different settings and parameters to generate unique compositions.


## Contribution Guidelines

Contributions to this project are welcome. If you find any issues or want to enhance the functionality, you can create a pull request with your changes. Please make sure to follow the existing coding style and provide detailed information about the changes you have made.

If you wish to contribute to this project, you can follow these guidelines:
1. Fork the repository.
2. Create a new branch for your contribution: git checkout -b feature/your-feature
3. Make your changes and commit them: git commit -m "Add your message"
4. Push the changes to your forked repository: git push origin feature/your-feature
5. Open a pull request, describing your changes and their purpose.Please ensure that your contributions align with the project's goals and follow the coding conventions and best practices.

## License
This project is licensed under the GNU License.

## Acknowledgement
We acknowledge the contributions of Vandana Yalla, M Kiranmayi, and V Hemachandana, who were the authors of the project report.

## Contact Information
If you have any questions or suggestions regarding this project, please feel free to contact the project maintainer.
