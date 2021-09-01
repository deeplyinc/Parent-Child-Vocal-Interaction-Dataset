# Deeply Parent-Child Vocal Interaction Dataset
---
## Summary
The interaction of 24 pairs of parent and child(total 48 speakers), such as <u>*__reading fairy tales, singing children’s songs, conversing, and others__*</u>, is recorded. The recordings took place in <u>*__3 different types of places__*</u>, which are *an anechoic chamber, studio apartment, and dance studio*, of which the level of reverberation differs. And in order to examine the effect of the distance of mic from the source and device, every experiment is recorded at <u>*__3 distinct distances__*</u> with <u>*__2 types of smartphone__*</u>, *iPhone X, and Galaxy S7*.

There were a parent and his/her child in a group, and each group was distinguished by a unique key(subject ID). Two speakers(speaker a(parent), speaker b(child)) were sitting on the floor(purple area in the pictures below), and asked to do 3 types of interactions, singing children's song, reading fairy tales, and singing lullabies. 

 **Recording environment** | **Studio Apartment(moderate reverb), Dance studio(high reverb),<br /> Anechoic Chamber(no reverb)** |
 :-:|:-:|
  **Device** | **[iPhone X(iOS)](https://en.wikipedia.org/wiki/IPhone_X), [Samsung Galaxy S7](https://en.wikipedia.org/wiki/Samsung_Galaxy_S7)** |
 **Recording distance from the source** | **0.4m, 2.0m, 4.0m** |
  **Volume(Sample)** | **\~ 282(~ 3) hours, ~ 360,000(~ 4,000) utterances, ~ 110(~ 0.4) GB** |
  **Format** | **wav/h5(16/44.1kHz, 16-bit, mono)** |
  **Language** | **Korean** |

 Studio Apartment | Dance studio | Anechoic Chamber |  
:-:|:-:|:-:|
![Studio](https://github.com/deeplyinc/Parent-Child-Vocal-Interaction-Dataset/blob/main/etc/StudioApartment.jpeg) | ![Dacne studio](https://github.com/deeplyinc/Parent-Child-Vocal-Interaction-Dataset/blob/main/etc/DanceStudio.jpeg) | ![Studio](https://github.com/deeplyinc/Parent-Child-Vocal-Interaction-Dataset/blob/main/etc/AnechoicChamber.jpeg) |

Refer to the dataset descriptions in 'docs' for detailed description and statistics of the full set of the dataset.

The dataset is a subset(approximately 1%) of a much bigger dataset which were recorded under the same circumstances as these open source samples. Please contact us(contact@deeplyinc.com) for the pricing and licensing.

## Dataset statistics
The illustrations below are the statistics about the Deeply Parent-Child Vocal Interaction Dataset. The first two are from the sample dataset, And the others are from the full dataset. To attain more insight about the dataset, please refer to the detailed description in 'docs' and 'Korea_Read_Speech_Corpus.json' in 'Dataset'.

The sample is a partial set of recordings from a single subject group(sub3004), which consists of 39-year-old female(parent, speaker a) and 5-year-old male(child, speaker b).

<p float="left">
  <img src="https://github.com/deeplyinc/Parent-Child-Vocal-Interaction-Dataset/blob/main/etc/fig0.png" width="400" />
  <img src="https://github.com/deeplyinc/Parent-Child-Vocal-Interaction-Dataset/blob/main/etc/fig1.png" width="400" />
</p>
<p float="left">
  <img src="https://github.com/deeplyinc/Parent-Child-Vocal-Interaction-Dataset/blob/main/etc/fig2.png" width="400" />
  <img src="https://github.com/deeplyinc/Parent-Child-Vocal-Interaction-Dataset/blob/main/etc/fig3.png" width="400" />
<p float="left">
  <img src="https://github.com/deeplyinc/Parent-Child-Vocal-Interaction-Dataset/blob/main/etc/fig4.png" width="400" />
  <img src="https://github.com/deeplyinc/Parent-Child-Vocal-Interaction-Dataset/blob/main/etc/fig5.png" width="400" />

## Structure
```
├── dataset
│   ├── AirbnbStudio
│   │   ├── sub30040a00000.wav
│   |   └── ...
│   ├── AnechoicChamber
│   │   ├── sub30042a00000.wav
│   |   └── ...
│   └── DanceStudio
│       ├── sub30041a00000.wav
│       └── ...
└── docs
    ├── Deeply\ Parent-Child\ Vocal\ Interaction\ Dataset_Eng.pdf
    └── Deeply\ Parent-Child\ Vocal\ Interaction\ Dataset_Kor.pdf
```

```
Parent_Child_Vocal_Interaction.json

{'AirbnbStudio': 
                {'sub30040a00000': {'label': 2,
                                    'subjectID': 'sub3004',
                                    'speaker': 'a',
                                    'age': 39,
                                    'sex': 0,
                                    'noise': 0,
                                    'location': 0,
                                    'distance': 0,
                                    'device': 0,
                                    'rms': 0.005859313067048788,
                                    'length': 1.521},
                  ...
                  },
...
}
```
### How to decode
_label_: {speaker a(parent): {0: singing, 1: reading, 2: other utterances},  
    speaker b(child): {0: singing, 1: reading, 2: crying, 3: refusing, 4: other utterances}}  

_Subject_ ID: Unique 'sub + 4-digit' key allocated to each subject group  

_Speaker_: unique key allocated to each indiivdual in the subject group.  

_Sex_: {0: Female, 1: Male}  

_Noise_: {0: Noiseless, 1: Indoor noise, 2: Outdoor noise, 3: Both indoor/outdoor noise}  

_Location_: {0: Studio apartment, 1: Dance studio, 2: Anechoic chamber}  

_Distance_: {0: 0.4m, 1: 2.0m, 2: 4.0m}

_Device_: {0: iPhone X, 1: Galaxy S7}  

_Rms_: Root mean square value of the signal  

_Length_: length of the signal in secods  

\* In polyphonic utterances, the categories, such as label, speaker,and sex, are longer than usual, because we've written the information of both speaker a and b in the same category.

For example, if speaker a(parent, male, 35 yo) sings and speaker b(child, female, 3 yo) trys to talk in a single audio file, *speaker* woudl be 'ab', *sex* would be '10'(male(speake a),female(speaker b)), and *label* would be'04'(singing(speaker a), other utterances(speaker b)) .

## License
Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)  
![Vue](https://github.com/deeplyinc/Parent-Child-Vocal-Interaction-Dataset/blob/main/etc/by-nc-nd.png)

## Other Deeply datasets
* **[Deeply Korean Read Speech Corpus](https://github.com/deeplyinc/Korean-Read-Speech-Corpus)**
  - Pairs of Korean reading the scripts with 3 text sentiments using 3 vocal sentiments. Recorded in 3 types of places, at 3 distinct distances, with 2 types of smartphone.
* **[Deeply Nonverbal Vocalization Dataset](https://github.com/deeplyinc/Nonverbal-Vocalization-Dataset)**
  - A human nonverbal vocal sound dataset by Deeply Inc.

## Contact
Tel:   (+82) 70-7459-0704  
Web:   http://deeplyinc.com/  
Email: contact@deeplyinc.com

