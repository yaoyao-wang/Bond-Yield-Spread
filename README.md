# 2 Year - 10 Year Bond Yield Rate SpreadIndex

## 1. What is the Spread?

The 10-year/2-year US Treasury spread is the difference between 10-year treasury constant maturity minus 2-year treasury constant maturity.

The width of the yield spread between these two securities helps to support predictions on whether the economy will experience a recession or a recovery over the course of the next 12 months.


## 2. What does the Spread tell you?

The 10-year/2-year US Treasury spread has a general tendency to signal the market’s  expectation of an upcoming recession or general downturn in growth.

Long-term Treasury yields are often used to examine the country's economic inflation, while short-term ones are often used to predict the country's interest rate. 

When the spread rises, the US economic risk increases, which is suitable for investing in bonds.  When the spread declines, the US economic risk decreases, which is suitable for investing in stocks.  

When the spread turns negative (referred to as the Inverted yield curve), the US economy will reach its peak, revealing that in the next 1 to 2 years, US stocks may have a significant decline, for example, in 1990,2000 and 2008.


## 3. Tradingview Pine Script

### · Step One: Initial Setting

    //@version=4
    //Step One: Initial Setting
    study("US 10 Year & 2 Year Treasury Spread", overlay = false)	

(1)Step one initial setting is the step we set up the general property, which includes “title”, “overlay”

(2) First, we need to set up the Pine Script version. Here, we are using the last version, version four.

(3) Then, we start to code the indicator’s general properties property. The double quote we type “US 10 Year & 2 Year Treasury Spread”, which is the title.

(4) “overlay equals true” means that the plot overlays the main chart. On the other hand, if “overlay equals false”, it means that the plot will show on the separate chart pane.

### · Step Two: Parameter Setting

    //Step Two: Parameter Setting
    us2y=security("US02Y", "D", close)
    us10y = security("US10Y","D",close)
    diff = us10y-us2y

(1)  The security function enables scripts to request data from symbols and/or resolutions other than the ones a script is running on. The symbol for 2 year US treasury rate is “US02Y” and the symbol for 10 year US treasury rate is “US10Y”. The “D” means the rate is calculated by “day” and “close” means the price is the closing price.

(2) Then we calculate the difference between 10-year US treasury rate and 2-year US treasury rate to get the spread

### · Step Three: Plotting

    //Step Three: Plotting
    plot(diff,color = color.red)

Now let’s plot the spread (difference) line and plot it with red. And we can get the result:

![](image/Spread.png)




