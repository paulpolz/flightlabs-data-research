# flightlabs-data-research
> The research data project based on the statistics of European flights collected from [FlightLabs Rest API](https://www.goflightlabs.com).

## The Research Process
1. Data Collector
    1. Get Countries
        - Filter a list of EU countries which are located on European continent and have EUR currency
    3. Get Airports
        - Collect a list of airports from the selected countries
    4. Get Flights
        - Select a start date
        - Select a period end date (+3-5 days from start_date) 
        - Per each airport:
            - Collect all the arrival flights to the selected EU airports
        - Save the data to JSON
2. Data Converter
    - Convert data from JSON to Pandas DataFrame
    - Filter the flights departured from the selected EU airports
    - Gather all the data and reassemble it to the feautures by columns for the further analysis
3. EDA

### The Research Limitations
- The period of gathered data is Jan 2023 - May 2023
- The flight routes coverage is limited by a variety of EU airports
- Per each airport an arrival data was collected as far as it includes the wider range of flight parameters and final flight status. Then this data was additionally filtered in order to leave only internal EU flight routes.
