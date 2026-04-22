Butterworth filter, LOW PASS filter, to cut off high frequency caused for example by impacts and vibrations.
The cutoff frequency must not be too low, otherwise you lose the peak frequency for the jumps, and not be too high otherwise you keep too much noise
Usually its used the filter at the order 2 or 4, moreover the result depends on the sampling frequency of the data

Library scipy.signal.butter

from scipy import signal

#PARAMETERS
fs=100.0 SAMPLING FREQUENCY OF THE DATASET
fc=15 CUTOF FREQUENCY
order=4

#FILTER COHEFFICIENTS
Wn = fc / (fs / 2)
b, a = signal.butter(order, Wn, btype='low')

#FILTERED DATA
filtered = DATA.filtfilt(b, a, acceleration)

use filtfilt for the  phase zero filtering, otherwise it will be casuaal

Note that sampling frequency affects the quality of the frequency, get worse when you get close to the Nyquist frequency.
