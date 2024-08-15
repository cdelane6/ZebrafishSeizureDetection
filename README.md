# ZebrafishSeizureDetection
Feature data recorded from Zebrafish epilepsy models.

This data set includes data extracted from recordings of PTZ-induced zebrafish epilepsy models. The data is contained within two .mat files. The two files correspond to different window sizes used when extracting the features. ZebrafishFeaturesDataset_v3 uses 4 second windows and ZebrafishFeaturesDataset_v3_1SecWindows uses 1 second windows. 

The labels for the data are created in two ways. The ANNLabels matrix made up of three columns of data with each row corresponding to a row in the Data matrix. Each column corresponds to a given class:
- 1st column = Seizure
- 2nd column = Neurotypical
- 3rd column = Artifact
  
The KNNLabels matrix has one column and each row corresponds to a row in the Data matrix. The value within each row of the matrix corresponds to a given class:
- 1 = Seizure
- 0 = Neurotypical
- -1 = Artifact

The Data matrix contains the feature data itself. The features are as follows from first column to last column of the Data matrix:
- Feature Name:	            Description
- Time Absolute Maximum:		  The maximum absolute value of amplitude from the time series.
- Time Variance:	            The variance of the amplitude from the time series.
- Time Root Mean Square:	    The root mean square value of amplitude from the time series.
- Time Sample Entropy:	      The sample entropy of the time series. 
- Time Energy:	              The signal energy of the time series. 
- Peak Frequency:	          The frequency with the maximum magnitude from the frequency domain view of the window.
- Average Power:	            The average magnitude across all frequency bins of the frequency domain view of the window.
- Delta Band Power:	        The power of the frequency band is from .5 to 4Hz of the frequency domain view of the window.
- Theta Band Power:	        The power of the frequency band is from 4 to 8Hz for the frequency domain view of the window.
- Alpha Band Power:	        The power of the frequency band is from 8 to 12Hz in the frequency domain view of the window.
- Beta Band Power:	          The power of the frequency band is from 12 to 30Hz in the frequency domain view of the window.
- Gamma Band Power:	        The power of the frequency band is from 30 to 50Hz in the frequency domain view of the window.
