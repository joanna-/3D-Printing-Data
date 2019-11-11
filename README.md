# 3D-Printing-Data

This repository contains data gathered from 3D printing machine MonkeyFab Spire. Each directory contains data samples gathered from different prints, some of them being fault. 

## Data usage 

You are free to use this data under *Creative Commons Attribution 4.0 International* license. If you use our data, please cite us as #TODO. 

## Data format

Generally, repository contains two types of data files:

* data from printer web interface 
* data from custom made measurement devices: accelerometer, gyroscope and ...

### Measurement devices characteristics

### Data format of web interface

### Data format of custom measurements

The data of custom measurements is saved in _csv_ files with no headers and standard comma delimeter. There are following columns:

* **0** - contains data id assigned as the relative time set up on the device
* **1-3** - 3-dimensional data from the first accelerometer (X, Y, Z axis respectively)
* **4-6** - 3-dimensional data from the second accelerometer (X, Y, Z axis respectively)
* **7** - tension measurements
* **8** - timestamp

In order to provide better understanding of the data, the following python script can be used to read data:
```python
import pandas as pd
df = pd.read_csv('accel.txt', names=['data_id', 'accel0X', 'accel0Y', 'accel0Z', 'accel1X', 'accel1Y',
                                'accel1Z', 'tension', 'timestamp'])
df['time'] = pd.to_datetime(df['timestamp'], unit='ms')
```

TODO: konwersja tension na przyspieszenie ziemskie?

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

 * _\four_towers_ - data related to printing towers model
 * _\monkeyfab_logo_ - data related to printing of monkeyfab logo with three monkeys figures

Data files are organised in the following subdirectories:

1. _proper_ - reference print
2. _plastic_lack_ 
3. _unstick_
4. _bowden_

And each of them contain two files: **.csv** one with data from custom-made measuremenet devices and **.json** file with data coming from the printer interface.

## Acknowledgments
**
Data presented in this repository was gathered, preprocessed and published as part of the project **LIDER/15/0144/L-7/15/NCBR/2016**. 
