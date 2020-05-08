# Covid19_EDA_and_Modelling
With the call for code, I wanted to analyze the rate at which the Coronavirus is spreading by country. Is it possible to develop a model that can predict the number of confirmed cases by day for all the countries in the world? If so I think itd be pretty cool to get my hands dirty with some code and data, tackling this complex problem.

First stage of the notebook will dive into just visualizing the number of confirmed cases in the world and by country. Are there any intersting observations to note and might there be information not previosuly known that would change modelling approach.

Second stage of the notebook I dive into data processing for both the LSTM model and the ARIMA model. 
    The Arima model needs a time series so I create the date objects and transform a copy of the original dataframe to be in long format. We need the dates to be row indexs not columns where we have dates for every country.
    The LSTM model is a little more complex in processing where because at the time of working on this project the time series would have only had 102 rows. To expand the data I make inputs of the sequence pairwise combinations (Date, Country_code). Every country will have confirmed cases for every date vastly increasing the number of periods available in our sequence.
    
Final stage and probably whats of most interest. MODELLING! woot. The ARIMA and LSTM both predict very well.
  The ARIMA is optimized using Grid search and the LSTM uses Adam with a RMSLE loss function.
  I highly suggest looking at the logic and architecture behind both models!
  
I also made a cool poster on my work for my school to be submitted into a data analytics conference, so if you want to just quickly skim, I highly reccomend going through the poster.
  
If you have any questions at all, please let me know!
