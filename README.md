# Ocean_wave_analysis_and_prediction_using_ARIMA_model
**DESIGN AND ANALYSIS OF ADVANCED UNDERWATER WIRELESS OPTICAL COMMUNICATION FOR OCEANOGRAPHIC APPLICATION**

We use wave monitoring buoys to continuously measure wave height, wave direction and wave period.
As a wave monitoring buoy floats up and down each passing wave, its motion (or heave) is measured and electronically processed.
Data from the wave monitoring buoys are transmitted to a nearby receiver station as a radio signal.

*Data Collection using Acoustic Transducers (Hydrophones)*

Field names are;
Hs - Significant wave height, an average of the highest third of the waves in a record (26.6 minute recording period).
Hmax - The maximum wave height in the record
Tz - The zero upcrossing wave period.
Tp- The peak energy wave period.
Dir_Tp TRUE- Direction (related to true north) from which the peak period waves are coming from.
SST - Approximation of sea surface temperature.

*Research Methodology*

Step 1: Wave Analysis using Regression
	This model is simple. I use data from last two months to predict (Hs) for the next step. I use walk forward validation with a sliding window of 3000 time steps (62.5 days). The model is tested for successive 200 time steps (10 hours). On average the difference between the predicted and actual data is about 31cm. The predictions and the actual data are also tested with a linear regression and found R value of 0.94. The results are very promising and could be enhanced further by optimizing the training window size.

Step 2: The prediction (forecasting) of significant wave height (Hs) using ARIMA
	In physical oceanography, the significant wave height (SWH or Hs) is defined traditionally as the mean wave height (trough to crest) of the highest third of the waves (H1/3). It is scientifically represented as Hs or Hsig, is an important parameter for the statistical distribution of ocean waves. The most common waves are lower in height than Hs. This implies that encountering the significant wave is not too frequent. However, statistically, it is possible to encounter a wave that is much higher than the significant wave. 

