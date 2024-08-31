### Bikeshare Data Analysis Program

#### Overview

This Python program allows users to explore bikeshare data from three major U.S. cities: Chicago, New York City, and Washington. The program lets users filter data by month and day of the week and then provides various statistics, including the most common travel times, popular stations, trip durations, and user demographics.

#### Features

1. **City Selection:** Users can choose between three cities: Chicago, New York City, and Washington.
2. **Filter by Month and/or Day:** Users can filter data by specific months (January to June) or days of the week.
3. **Comprehensive Statistics:**
   - Most frequent times of travel.
   - Most popular stations and trip combinations.
   - Trip duration statistics.
   - User demographics, including gender and birth year (if available).

#### Dependencies

- **Python 3.x**
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Time**: For measuring the time taken for calculations.

You can install the required packages using pip:

```bash
pip install pandas numpy
```

#### How It Works

1. **City Selection:**
   - Users are prompted to select a city by entering a number (1 for Chicago, 2 for New York City, 3 for Washington).

2. **Filter Selection:**
   - Users can choose to filter the data by month, day, both, or none.
   - If filtering by month, users select a month from January to June.
   - If filtering by day, users select a day from Monday to Sunday.

3. **Data Loading and Filtering:**
   - The program loads the relevant CSV file for the selected city.
   - It filters the data based on the selected month and/or day, if applicable.

4. **Statistical Analysis:**
   - The program calculates and displays various statistics, including:
     - Most common travel times (month, day, and hour).
     - Most popular start and end stations.
     - Total and average trip duration.
     - Counts of user types, gender distribution, and birth year statistics.

5. **Restart Option:**
   - After displaying the statistics, the user is asked if they want to restart the analysis with different filters.

#### Files

- `chicago.csv`: Dataset for Chicago bikeshare data.
- `new_york_city.csv`: Dataset for New York City bikeshare data.
- `washington.csv`: Dataset for Washington bikeshare data.

#### Functions

1. **get_filters():** 
   - Prompts the user to select a city, month, and day for filtering the data.

2. **load_data(city, month, day):** 
   - Loads the city-specific data and applies filters based on user input.

3. **time_stats(df):** 
   - Displays statistics on the most frequent times of travel.

4. **station_stats(df):** 
   - Displays statistics on the most popular stations and trip combinations.

5. **trip_duration_stats(df):** 
   - Displays total and average trip duration.

6. **user_stats(df):** 
   - Displays statistics on bikeshare users, including user types, gender, and birth year.

7. **main():** 
   - The main function that orchestrates the entire program, managing user input, data loading, and displaying statistics.

#### How to Run the Program

1. Clone or download the repository containing the program and CSV files.
2. Make sure the required libraries are installed (Pandas and NumPy).
3. Run the program using Python:

```bash
python bikeshare.py
```

4. Follow the on-screen prompts to select a city, filter options, and view the statistics.

#### Sample Output

```bash
Hello! Let's explore some US bikeshare data!

Which city report would you like to see? 
1. Chicago   2. New York City    3. Washington : 
Enter number: 1

Would you like to filter the report based on month, day, both or none? 
Type 'None' for no filter: 
Month

Which month's report would you like to see? 
Choose number 1 to 6 (e.g. 1 = Jan, 2 = Feb... 6 = Jun): 
2

Calculating The Most Frequent Times of Travel...
Most common month of Travel: 2
Count: 2345

Most common day of Travel: Wednesday
Count: 345

Most common hour of Travel: 17
Count: 456

...

Would you like to restart? Enter yes or no.
```

#### Assumptions and Limitations

- The data files for Chicago, New York City, and Washington are pre-loaded and must be present in the same directory as the script.
- The program only supports filtering by months January to June.
- Washington's dataset does not include 'Gender' and 'Birth Year' columns, so relevant statistics are not displayed for this city.

#### Potential Improvements

- Add support for additional cities and extend the month filter beyond June.
- Implement more sophisticated data imputation techniques for missing values.
- Enhance the user interface for better interactivity.
