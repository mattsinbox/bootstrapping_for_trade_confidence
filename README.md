# Project Motivation
While looking at option prices on the eur/usd that expire in about 12 days, the straddle prices looked very cheap.  https://www.investopedia.com/terms/s/straddle.asp.  The implied volatility for these options was 3%.  I wanted to use historical data to see if the straddle price was cheap by sampling through the data and picking 12 day periods.  By sampling, I could then build a confidence interval and see the percentage of times the eur/usd moved more than the straddle price.  I thought this could be helpful and applied when evaluating any asset's straddle price.   

# sampling_through_chaos

Notebook is designed to go through basic closing prices and determine a straddle price through sampling.  Since daily markets moves 
show dependency, in order to sample moves, one must look at groups of dates.  This notebook randomly samples datea and then looks 
ahead X days and figures the move.  It then takes this sample Y iterations.  The mean of these samples
becomes a good approximation for an option straddle price.  It also allows a confidence interval around the current traded
option price price by comparing how many of the samples fell above or below the current price.  

# Better wrangling of the data is needed 
Alternate data is needed.  FX futures prices have a roll, which can skew daily moves.  Should use historical spot data when 
building models.  

