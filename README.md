# VeReMi-Attack-Detection-Master-Thesis
This repository contains the full paths for the VeReMi post-attack master’s thesis.
Here is a short paragraph you can use to share the Google Drive link for accessing the data:

You can access the dataset files here: https://drive.google.com/drive/folders/11XiBYONftrVmJNJ8YsNVHLmAQIKXq2Zu?usp=sharing.
The folder contains the following CSV files: ConstPosOffsetFullPathes.csv, EventalStopFullPathes.csv, RandomPosFullPathes.csv, 
and RandomPosOffsetFullPathes.csv. Note that ConstPosFullPathes.csv (without "Offset") is not present because it was deleted by mistake.
Use this repository to handle the datasets: https://github.com/muradialotabi/Data-Pre-Processing.git.
All available files can be downloaded directly from Google Drive.


VeReMi Dataset Structure :

The VeReMi dataset is organized into several subsets representing different simulation scenarios. Each subset includes a ground truth (GT) file and multiple message log files containing received message data.

Each message log file represents a log of messages received by a vehicle at specific timestamps. These files record what each vehicle received during the simulation.

The ground truth file contains information about all transmitted messages during a simulation and identifies which messages were sent by attackers. The ground truth includes all sending events from a single simulation, while the message logs contain the corresponding reception events.

Each entry in the message log files contains the following information:
	•	reception timestamp
	•	claimed transmission time
	•	claimed sender ID
	•	simulation-wide unique message ID
	•	position vector
	•	speed vector
	•	received signal strength indicator (RSSI)
	•	position noise vector
	•	speed noise vector
	•	module ID

The module ID originates from the VEINS simulation framework and is used to identify the simulated modules, such as vehicle components, base stations, or the SUMO connector.

In addition, the ground truth file is updated whenever a message is transmitted by any vehicle. This file includes:
	•	transmission time
	•	sender ID
	•	attacker type
	•	message ID
	•	actual position vector
	•	actual speed vector

The attacker type is set to 0 for legitimate vehicles, while other values represent different attacker behaviors. Typically, there may be more than one attacker in a simulation scenario.

Each subset therefore provides both the transmission ground truth data and the corresponding received message logs, allowing researchers to analyze vehicle communication behavior and detect malicious messages
