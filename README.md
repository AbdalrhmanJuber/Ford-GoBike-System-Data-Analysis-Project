# Ford GoBike System Data Analysis Project

## Project Overview
This project analyzes the Ford GoBike System data from February 2019, exploring usage patterns and characteristics of the bike-sharing service in the San Francisco Bay Area. The analysis is divided into two main parts:

1. **Exploratory Data Analysis**: A systematic exploration of the dataset using Python visualization libraries, starting with univariate analysis and building up to multivariate relationships.

2. **Explanatory Data Analysis**: A focused presentation highlighting key findings from the exploratory analysis with polished visualizations that communicate insights effectively.

## Dataset
The Ford GoBike System dataset contains trip data from February 2019, with information about:
- Trip duration
- Start and end times
- Start and end station locations and IDs
- User types (Subscriber or Customer)
- User demographics (birth year, gender)
- Bike ID and program information

After cleaning, the dataset contains 182,995 bike trips.

## Files in Repository
- `201902-fordgobike-tripdata.csv`: The raw dataset
- `Part_I_exploration.ipynb`: Jupyter notebook containing the exploratory data analysis
- `Part_I_exploration.html`: HTML export of the exploratory analysis
- `Part_II_slide_deck.ipynb`: Jupyter notebook containing the explanatory presentation
- `Part_II_slide_deck.html`: HTML export of the explanatory presentation
- `README.md`: This file documenting the project

## Tools & Libraries Used
- Python 3.x
- Pandas: Data manipulation and analysis
- NumPy: Numerical computing
- Matplotlib: Basic plotting and visualization
- Seaborn: Statistical data visualization
- Math library: For Haversine formula to calculate distances

## Analysis Process

### Part I: Exploratory Data Analysis

#### Preliminary Wrangling
- Loaded and inspected the dataset
- Handled missing values
- Created new features:
  - Day of week, hour of trip
  - Trip duration in minutes
  - Trip distance in kilometers using Haversine formula
  - User age from birth year
- Filtered outliers (trips < 1 minute or > 3 hours)

#### Univariate Exploration
- Analyzed trip duration distribution
- Explored user types distribution (Subscribers vs. Customers)
- Examined gender distribution
- Investigated trip timing throughout the day

#### Bivariate Exploration
- Compared trip duration by user type
- Analyzed trip counts by day of week
- Examined relationship between trip duration and distance
- Explored hourly patterns by user type

#### Multivariate Exploration
- Investigated trip patterns by day of week, hour, and user type
- Analyzed how age and gender affect trip duration
- Explored station popularity by time of day and user type

### Part II: Explanatory Analysis
For the explanatory phase, we focused on five key findings and created polished visualizations:

1. **User Types and Usage Patterns**: 
   - Illustrated the distinct behaviors of Subscribers (89.3%) vs. Customers (10.7%)
   - Showed how Subscribers take shorter trips (median: 8.2 min) than Customers (median: 13.1 min)

2. **Temporal Patterns**:
   - Highlighted weekday commuting patterns with morning and evening peaks
   - Contrasted with weekend usage that's more evenly distributed throughout the day

3. **User Type, Time, and Purpose**:
   - Demonstrated how user types and trip timing are interconnected
   - Showed the shift in Subscriber behavior from weekday commuting to weekend leisure

4. **Trip Characteristics**:
   - Analyzed trip distance distributions by user type
   - Examined the relationship between distance and duration, including average speeds

5. **Station Popularity**:
   - Identified the most popular stations and their usage patterns
   - Showed how station popularity varies based on location type and user demographics

## Key Findings

1. **Dual Purpose System**: The Ford GoBike system serves:
   - As a **commuting tool** for regular Subscribers (89% of users)
   - As a **leisure activity** for one-time Customers (11% of users)

2. **Distinct Temporal Patterns**:
   - **Weekday commute peaks** in morning (8-9 AM) and evening (5-6 PM)
   - More evenly distributed **weekend leisure usage**

3. **Different User Behaviors**:
   - Subscribers take **shorter, faster, more direct trips** (median: 8.2 min, 1.4 km)
   - Customers take **longer, more leisurely trips** (median: 13.1 min, 1.7 km)

4. **Station Usage Varies**:
   - Stations near transit and business districts serve primarily Subscribers
   - Stations in tourist and mixed-use areas have higher proportions of Customers

## Conclusions

The analysis revealed that the Ford GoBike System effectively serves two distinct purposes: daily commuting for regular subscribers and leisure/tourism for casual customers. This insight could help system operators optimize bike distribution, station capacity, and marketing strategies.

Understanding these diverse usage patterns could also inform future infrastructure planning, helping to ensure that the bike-sharing system continues to meet the needs of both user groups effectively.

## How to Run the Analysis
1. Ensure you have Python 3.x installed with the required libraries
2. Open the Jupyter notebooks in a compatible environment
3. Run the cells sequentially to reproduce the analysis

Alternatively, view the HTML exports to see the complete analysis with all visualizations.
