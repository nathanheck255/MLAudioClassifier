  <h3 align="center">Automatic Drum Sample Labelling with Machine Learning</h3>

  <p align="center">
    Classifying short recordings of percussion instruments with a CNN trained on spectral features.
    <br />
    <br />
    <br />
    <a href="#usage">View Demo</a>
    ·
    <a href="https://github.com/uf-eel6825-sp23/final-project-code-nathanheck255/issues">Report Bug</a>
    ·
    <a href="https://github.com/uf-eel6825-sp23/final-project-code-nathanheck255/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#dependencies">Dependencies</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#authors">Authors</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

This is my final project for the EEL6825 Pattern Recognition course at the University of Florida. I developed a neural network classifier to identify the percussion instrument present in an audio file. This will be useful for music producers who, rather than recording instruments with a microphone, might be working with prerecorded samples of a drum kit. Running the code here will label all the files in a library of one-shot drum recordings and organize them into folders based on what instrument is identified. To train and test this model I gathered a custom dataset from free sample packs I found on the internet, either through individual producers or music software companies. The neural network architecture I am using is based on a paper by Mahanta et al. published in 2021. (1) I am also using an autoencoder to extract features from the spectrograms of the audio files, which I based on a design from a blog post on the Keras website. (2)

For more information, please see my paper on this subject:

[Automated Classification of Drum Sounds for Modern Music Production](https://github.com/nathanheck255/MLAudioClassifier/PatternRecognitionProjectReport.pdf)

See my video explanation here:
https://youtu.be/V31PLUZOtdc

or any of these other resources which informed my implementation of this model:

(1) S. Mahanta, A. Khilji, P. Pakray, “Deep Neural Network for Musical Instrument Recognition Using MFCCs,” in Computation and Systems, vol. 25, pp. 351–360, Nov. 2021

(2) F. Chollet, “Building Autoencoders in Keras,” The Keras Blog, 14-May-2016. 

(3) K.D. Martin, Sound-Source Recognition: A Theory and Computational Model, May 1999.


<!-- GETTING STARTED -->
## Getting Started

Please clone this repository first, and then before running any of the code you must unzip the training data and test data archive files. The test data is small enough that I could include it directly in this repo, but the training data is too large, so I had to attach it to the assignment on Canvas. You'll have to download it from there and then copy it inside this repo. 


### Dependencies

The two main libraries I used in my model design were Keras for the neural network architecture and Librosa for the audio processing. I used a bunch of other libraries too like Numpy, MatPlotLib, etc. These are all fairly popular, so you should not have to do any special installations before running my code. Just make sure you run it on HiperGator using the UFRC Python-3.10 kernel and you won't have any problems. 


### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/uf-eel6825-sp23/final-project-code-nathanheck255.git
   ```

But if you are using HiperGator then you might need to clone with ssh:
   ```sh
   git clone git@github.com:uf-eel6825-sp23/final-project-code-nathanheck255.git
   ``` 
   
2. cd into the repo

3. Copy the training data files from Canvas into the repo:
TrainingData.zip and mfcc_train_data.json

<!-- USAGE EXAMPLES -->
## Usage

This project is made up of 4 Jupyter notebooks. I have included some saved, pretrained models in here so you could technically just run the Model_Evaluation.ipynb notebook if you want to get straight to the results. But if you want to run through every part of the model, this is the sequence that they should be executed:

1. MFCC_Feature_Extractor.ipynb
2. Model1_Train.ipynb
3. Model2_Train.ipynb
4. Model_Evaluation.ipynb

I also checked in a fifth notebook called PracticalDemo.ipynb, which I used to demonstrate the model's capabilities in my video presentation.

<!-- ROADMAP -->
## Roadmap

This model is only capable of reliably classifying three classes of instruments: kick drum, snare drum, and hi-hat. In the future I would like to improve on this model by trying out other neural network architectures and feature extraction methods. I will keep experimenting with that and pushing updates to this repo as I make progress. 

As a long term goal for this project, I could see this running on the back end of a virtual instrument sampler plugin. As a first step towards that, I could try to write some scripts that can be called my digital audio workstation upon startup to scan my sample library and pass them through a pretrained model.

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.


<!-- Authors -->
## Authors

Nathan Heck - [@hexmusiclabs](https://www.instagram.com/hexmusiclabs/) - nathan.heck@ufl.edu - hexmusiclabs@gmail.com

Project Link: [https://github.com/uf-eel6825-sp23/final-project-code-nathanheck255](https://github.com/uf-eel6825-sp23/final-project-code-nathanheck255)


<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

You can acknowledge any individual, group, institution or service.
* [Catia Silva](https://faculty.eng.ufl.edu/catia-silva/)
* [The Keras Blog](https://blog.keras.io/)
* [UF ECE Department](https://www.ece.ufl.edu/)

## Thank you

