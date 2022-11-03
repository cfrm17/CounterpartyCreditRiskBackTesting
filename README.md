# Counterparty Credit Risk Back Testing

Backtesting is the comparison of forecasts to realised outcomes. This comparison is either the comparison of a distribution with a single realised value at a point in time, as for market risk factor or exposure distribution backtesting, or the comparison of a single predicted value against some realised value at a point in time, as for backtesting EPE or pricing models.

VaR backtesting is a particular example of the former comparison of testing forecast distributions against realised outcomes. This paper argues that the VaR approach is inappropriate for backtesting the internal models used for counterparty credit risk calculations and suggests approaches that are more suitable.

The methodologies we discuss are based on comparison between the internal model forecasted probability distribution of exposure at various time horizons (calculated for representative counterparty portfolios) and the actual exposures that would have occurred on each portfolio at each time horizon by using in computation historical data on movements in market risk factors.

A forecast distribution of market risk factors or exposures has a number of properties. Forecasts are initialised at a particular point in time. The initialisation point is the date and time that a forecast is launched or issued.

Each forecast distribution has a time horizon, the time between initialisation and the realisation of the forecast. A forecast initialised on January 1st that realises on January 15th has a 14 day time horizon, a two week forecast. Note that forecasts with different time horizons can have the same initialisation date, ie two week and four week forecasts that realise on 15th and 29th January respectively would both have been initialised on the same date, 1st January.
 
Backtesting is a statistical test with the significance of any result depending on the amount of data used. A backtesting data set is a set of forecasts and the corresponding realisations of those forecasts, ie what actually occurred. This backtesting data set can be put together in a number of ways.
 
Backtesting using data from a single counterparty over a short period of time may not produce a meaningful conclusion about the quality of the EPE models and its sub-components used to generate that exposure. Firms with advanced model permission have addressed the data requirement problem by aggregating backtesting data across a number of dimensions. The possible dimensions are discussed below.

The backtesting data set can be aggregated over time, over trades/risk factors or over both time and trades/risk factors. The time period over which data is aggregated is referred to as the observation window. There are a number of methodologies for generating a backtesting data set over a given observation window. A selection of frequently used methodologies are set out below.

The backtesting data set is constructed by taking, say, 1-week time horizon forecasts initialised on dates 1 week apart. Note that as the time horizon increases to the levels required by IMM backtesting, the effective period of the observation window must increase in order to maintain the same number of data points. Large observation windows are required in order to achieve significant results and as a result the evaluation of model performance may be determined over a range of market conditions.

There are two types of models in trading: valuation model and risk model. Valuation model is used for compute present value and sensitivities, such as https://finpricing.com/lib/EqBarrier.html

