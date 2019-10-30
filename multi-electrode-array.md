---
layout: page
title: Multielectrode Array (MEA)
permalink: /multi-electrode-array/
---

## Multi Electrode Array

### Hardware info:  


System  
BioCam X  
Nr. Channels: 4095  
Sampling rate: 18 kHz  
MEA Chip: HD-MEA Arena  
Electrode size 21 µm2  
Electrode Area: 2.67 mm2  
Recording Software: Brainwave X or Brainwave 4  
Spike sorting algorithm: HS2 by Matthias Hennig  

***

### Basic maintenance protocols:

Cleaning:

Before recording:
Rinse with 100% alcohol and wash with DD water

After recording:  
Clean with DD water  
Alconox 1 over night  
Wash with DD water afterwards
Chips should stay dry except for the area with the electrodes, especially electrical contacts need to stay clean as they are very sensitive to oxidation or dirt.  
Chips should be handles with gloves and be stored in their boxes.

***

### Recordings:

Switch the MEA on using a button on the back right.
Recordings can be done using Brainwave X or Brainwave 4. (Note that changing the software requires a driver update of the MEA which takes about 5 minutes)  

Chips are inserted after pressing the button on the left side to the middle position. Once the chip is inserted press the button to the full down position. Don’t press the chip in if you encounter a resistance but check if the button is in the right position.  

Don’t run a recoding when the ground electrode is not inserted into the recording solution. Before removing the chip make sure the recoding has been stopped (otherwise the MEA can get damaged).
Change the amplification bias in the software in order to calibrate the chip or use the “auto-calibration” function.   

Don’t set the bias below -300, this could damage the chip.

***

### After recording:

Use the HS2 spikesorting script to sort the spikes in the recording file. Log into “Analysis” account on Windows (press windows+L). Start Anaconda, change environment to HS2. Start spyder. The script “biocam detect” should pop up on start.  

The script searches the folder for subfolders named (Phase_00, Phase_01 etc.) store the recording files of the recording in these subfolders. The script will go through the subfolders and analyse the files in them. (Note that the script breaks if there are other files in the subfolders). Once the script is finished a file with the sorted spikes can be found in the subfolders.

***

### Perfusion system

The perfusion system needs to be changed weekly.

Check the grounding before using the perfusion system (red cable attached to the metal tube). If the grounding is not connected you will likely encounter ground loop noise.

Give all bottles used to make the perfusion solution to sterilization after every second recording, otherwise algae will start to grow and poison the perfusion solution.
