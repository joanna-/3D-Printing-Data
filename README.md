# 3D-Printing-Data

This repository contains data gathered from 3D printing machine MonkeyFab Spire. Each directory contains data samples gathered from different prints, some of them being fault. The data 

## Data usage 

You are free to use this data under *Creative Commons Attribution 4.0 International* license. If you use our data, please cite us as #TODO. 

## Data format

Generally, repository contains two types of data files:

* data from printer web interface 
* data from custom made measurement devices: accelerometer, gyroscope and ...

### Measurement devices characteristics

### Data format of web interface

### Data format of custom measurements

## Data files

Reference properly made print:

<img src="docs/proper.jpg" alt="proper print image" height="250"/>

The files contain data from the following faulty situations:

1. Finish of 3D printing plastic.

<img src="docs/plastic_lack.jpg" alt="plastic lack image" height="250"/>

2. Bowden tube fallout.

3. Wrong retraction setup.

<img src="docs/wrong_retraction.jpg" alt="wrong retraction image" height="250"/>

4. 

5. Unsticking of the printed model.

<img src="docs/unstick.jpg" alt="unstick image" height="250"/>

## Repository organization

The directory structure is as follows:

  \four_towers - data related to printing towers model
  \monkeyfab_logo - data related to printing of monkeyfab logo with three monkeys figures

Data files are organised in the following subdirectories:

1. _proper_ - reference print
2. _plastic_lack_ 
3. _unstick_
4. _bowden_

And each of them contain two files: **.csv** one with data from custom-made measuremenet devices and **.json** file with data coming from the printer interface.

## Acknowledgments
**
Data presented in this repository was gathered, preprocessed and published as part of the project **LIDER/15/0144/L-7/15/NCBR/2016**. 
