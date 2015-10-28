# v-03_sound-patterns

A max/msp patch that generates squared images from level values of an audio samples. The patch takes into account the following 3 values:

 - Length, in minutes
 - BPM
 - Signal's amplitude

Signal's amplitude values are converted on a range going from 0 to 255. Each value generates a square, which appearence goes from black (0) to white (255). Width and height of the image are chosen to be identical, the density of suqares filling the area is calculated by multiplying the audio file's length, by the BPM of the file. Needless to say, the audio source has to have a BPM to be able to follow this rule. Alternatively the BPM value can be used to set the density in an arbitrary way, for example if the file is 3 minute long and BPM is set to 3, the area will be filled with 9 (3*3) squares.

## Examples 
The following images have been generated using 3 popular music songs. In some cases, like Modugno's Vecchio Frak you'll be able to see very few white suqares. While this song is very quiet, it doesn't mean that it's mostly silent, simply most of the values are very low and generate a very dark output that we perceive as black.

![alt tag](https://github.com/lucaderosso/v-03_sound-patterns/blob/master/exports/hires/HIRES_188_313_84_Rihanna%20Kanye%20West%20Paul%20McCartney%20-%20four-five%20second%20.mp3.jpg)

[ABOVE] *Rihanna, Kanye West, Paul McCartney,* **FourFiveSecond** | Tempo: 100BPM | Length: 3:08

![alt tag](https://github.com/lucaderosso/v-03_sound-patterns/blob/master/exports/hires/HIRES_238_436_55_Domenico%20Modugno%20-%20Vecchio%20Frak.mp3.jpg)
 
[ABOVE] *Domenico Modugno,* **Vecchio Frak** | Tempo: 120BPM | Length: 3:58

![alt tag](https://github.com/lucaderosso/v-03_sound-patterns/blob/master/exports/hires/HIRES_376_846_23_The%20Chemical%20Brothers-It%20Began%20In%20Afrika.mp3.jpg)

[ABOVE]  *The Chemical Brothers,* **It Began In Afrika** | Tempo: 135BPM | Length: 6:16

## Patch

To use the patch follow this instructions: 

- 1: Indicate track's BPM.
- 2: Load track to generate image from.
- 3: Print image from track.

Options:
Lo-Res / Hi-Res: Change resolution to plrint a small (500 * 500px) or a big (2500 * 2500px) image
Contrat: increases the value assigned to each square. While this allows to see more "invisible" elements, it also fakes the captired values.

![alt tag](https://github.com/lucaderosso/v-03_sound-patterns/blob/master/ldr-03_sound-patterns.png)
