# Radialpoint Relay Programming
Our assignments are grouped around a bike rental system.

## Dataset Analysis
Understanding usage patterns is central in achieving a good bike rental service.  Using the provided historical data help the bike rental administrators answer these questions.

### Historical Data

> The data is provided as a comma separated value (CSV) file named *hour.csv*.  It contains hourly usage of the bike rental system over a two-year period.

*Fanaee-T, Hadi, and Gama, Joao, Event labeling combining ensemble detectors and background knowledge, Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg.*

Each column should be interpreted as follows:

- instant: record index
- dteday : date (from January 1st 2011 to December 31, 2012)
- season : season
    1. winter
    2. spring
    3. summer
    4. fall
- yr : year (0: 2011, 1:2012)
- mnth : month (1 to 12)
- hr : hour (0 to 23)
- holiday : whether day is holiday or not
- weekday : day of the week
- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
- weathersit : (can be interpreted as best [1] to worst [4] temperature conditions)
    1. Clear, Few clouds, Partly cloudy
    2. Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
    3. Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
    4. Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
- temp : Normalized temperature. The values are divided to 41 C (max)
- atemp: Normalized feeling temperature. The values are divided to 50 C (max)
- hum: Relative humidity.
- windspeed: Normalized wind speed. The values are divided to 67 km/h (max)
- casual: count of casual users
- registered: count of registered users
- cnt: count of total rental bikes including both casual and registered


### Instructions
For this first set of questions you need to provide a command line app or a script in your **preferred programming language** that will accept as a parameter the historical data in its **original CSV format** and output the answers on the console.  Please document any step that may not be obvious in order to run your app.  In the following, the provided numbers are only examples.

Help understand the bike usage patterns by answering these questions:

0. (10%) What is the **maximum hourly** bike rental (i.e. column cnt) over the 2-year period? Output the date and hour with the format `YYYY-mm-dd HH:mm:ss` where hour values are from 0 to 23 and the number of bike rentals:
    - 2011-01-26 16:00:00 with 5 rentals

0. (10%) What are the days and times where the bike **hourly** rental was equal or more than 90% of the above maximum hourly rental?  Output each result on one line containing the date and time in the format above with the number of bike rentals in chronological order:
    - 2011-01-26 16:00:00 with 5 rentals
    - 2011-01-27 17:00:00 with 6 rentals
    - 2012-02-11 09:00:00 with 2 rentals

    **Observe:** the results will show an increase in bike rental in 2012.

0. (15%) What is the **maximum daily** bike rentals over the 2-year period?  You can assume that the daily rentals is the sum of the hourly rentals.  Output the date and the number of rentals on that day:
    - 2011-01-26 with 100 rentals

0. (15%) What are the days where the bike **daily** rental was equal or more than 90% of the above maximum daily rental?  Output each result on one line containing the date in the format above and the rentals in **increasing order**:
    - 2011-01-27 with 90 rentals
    - 2011-02-11 with 97 rentals
    - 2011-01-26 with 100 rentals

    **Observe:** fall is a great season for biking!

0. (15%) How does the weather conditions impact the bike usage?  Give the **average hourly usage** for each of the weather conditions
    - weather: 1 average hourly rentals: 234
    - weather: 2 average hourly rentals: 23
    - weather: 3 average hourly rentals: 105
    - weather: 4 average hourly rentals: 403

0. (15%) How does the season impact the bike usage?  Give the **average daily usage** for each of the four seasons:
    - spring average rentals: 56
    - summer average rentals: 90
    - fall average rentals: 97
    - winter average daily rentals: 40

0. (20%) There are plenty more trends and observations we can learn from this data set.  Drill into the data and tell us what you found.  Is usage greater on holidays or on working days?   Does bike usage differ greatly from casual users and registered ones?    Are the weather conditions impacting the service usage more than the seasons?  What are the best signals (weather, temperature, holiday, …) to predict the rental on any given day?
