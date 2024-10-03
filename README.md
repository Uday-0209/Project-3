# Couple-defect-detection
In the test rig, one of the defects we observed is a failing coupling. I developed a model that can predict whether the coupling is in good or bad condition based on vibration data.

The methodology to develop model as follows:
1) First, I collected the vibration data when the coupling was both in bad and good condition. The data came from sensors mounted near the drive system and at the nut.
2) The data was then transformed into STFT format and saved according to the respective condition.
3) The model was built using an MLPClassifier, and I whipped up a LabVIEW program to verify it in real-time. LabVIEW was integrated with a Python engine for this.
4) Once real-time data is acquired, it gets converted to STFT format and passed over to the Python program. There, we apply PCA, do the necessary processing, and predict the condition.
5) This whole process runs every 5 seconds on a loop.
