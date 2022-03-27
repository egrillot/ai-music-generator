# ai-music-generator

## Introduction

In this project, we set ourselves the goal of exploring as many possibilities as possible for generating music and interpreting our models as best we could. Several approaches are proposed, ranging from predicting the most likely note after a given sequence of notes to generating a piece of music with several instruments. The two main difficulties were the following: 
* The high dimensionality of the problem which led us to use very large datasets
* The generation of a real new melody and not just a sequence of redundant notes

## Dataset

We worked with the data: [Lakh Pianoroll Dataset](https://salu133445.github.io/lakh-pianoroll-dataset/). We kept the cleaned data "lpd_5/lpd_5_cleansed". We can find in this dataset 21,425 multitrack pianorolls. From this data, we extracted for each piece the tracks of 5 instruments where possible. These instruments are the piano, the guitar, the bass, the strings and the drums. Thus, a song is represented by a dictionary whose keys are the instrument names and whose values are the tracks. If an instrument is not represented, we assign the value "None" in the dictionary, otherwise the track is represented by a matrix of size n x 128 where n corresponds to the number of time steps in the song and 128 the number of possible notes.
