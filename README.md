# Music Creation GAN
## COMP 432 Fall 2020
## [Natalia Whiteley](https://github.com/nat-w) 40044353 and [Michael Naccache](https://github.com/NoDevicesFound) 29794840

---

# Intro
This is a deep-learning model based on the WaveNet model by Google Deepmind used to create music from existing songs in a genre. Some example songs the model created are included in the *results* folder.

---

# Prerequisites
You will need to have all of these python libraries installed for this project to run.

* Music21
* Numpy
* Matplotlib
* Seaborn
* Scikit-Learn
* Tensorflow

---

# Files Included
* **Music_GAN.ipynb**       -- notebook for the project
* **midi_files**            -- the dataset of midi files with a sub-folder for each genre
* **model_checkpoints**     -- folder that contains saved model weights
* **results**               -- folder that contains created midi files
    * **result.mid**        -- the midi file created by the model
    * **result-*.mid**      -- saved results from the model on previous runs

---

# How to Run
Open the notebook and run all the cells to generate a midi file called *result.mid* in the **results** folder. You can change the genre the model is trained on by changing the *TRAIN_GENRE* constant to one of the strings in the *GENRES* list above it.

---

# Notes/Warnings
* The notebook contains outputs and trained models from running the project on the Classical genre.
* Some genres have many songs in them and will take a long time to import and train. Zelda and original are good genres to choose that don't take too long.
* If you change any of the training data or hyperparamters of the model, you **must delete** all the checkpoints in the *model_checkpoints* folder or else the model will not re-train and will break in the prediction step.

---

# Sources
 This is the paper for the WaveNet model we based our model on.
* https://arxiv.org/pdf/1609.03499.pdf

We used this article for help with the midi import and export and for inspiration for a WaveNet model in Tensorflow.
* https://www.analyticsvidhya.com/blog/2020/01/how-to-perform-automatic-music-generation/

This isn't really a source we used, but it a fun example of all the instruments and notes in midi files. It's a good reference to understand midi music.
* https://jazz-soft.net/demo/GeneralMidi.html