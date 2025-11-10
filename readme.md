# Data Visualization - Ford GoBike (Bike Shares)


## Dataset
The dataset, **2017-fordgobike-tripdata.csv**, was downloaded from Ford GoBike and is licensed by Ford GoBike. It contains **519,700** trip records with **15 features**, including trip times, station locations, and rider attributes. Each trip has both a start and an end station.
During exploration, I noticed that a large portion of trips originated from a small set of popular stations. To focus the analysis and reduce noise, I filtered the data to include only the **top 8 start stations** with the highest trip counts.
In addition, the Ford GoBike program officially launched on **June 28, 2017**, so the data for June represents only a partial month. To avoid bias from this incomplete period, I excluded June trips from the analysis.
Therefore, all subsequent analysis is based on this **subsetted dataset** (top 8 start stations, July–December 2017).



## Summary of Findings
**Univariate Exploration:**
The number of trips shows a gradual decline as the weather becomes colder. Within a typical day, trip counts peak during the morning and late afternoon commute hours and drop at night. Ridership is also higher on weekdays than on weekends, which is consistent with work-related usage. As expected, there are more trips by subscribers than by casual customers, given the pricing structure of the system.

In terms of rider demographics, male riders take roughly three times as many trips as female riders, which is a noticeable imbalance and worth further investigation. Most riders fall in the 30–40 year age range, and the typical trip duration is around 650 seconds (about 11 minutes).


**Bivariate Exploration:**
The relationship between rider age and trip duration shows a **slightly negative correlation** — as age increases, trip duration tends to decrease, but the effect is small.

After focusing on the top 8 start stations, an interesting temporal pattern appears: **about half of these stations peak in the morning** (likely commute-oriented trips), while **the other half peak in the afternoon**, which may reflect return commutes or leisure rides.

As seen in the univariate analysis, **weekdays consistently have more trips than weekends**, reinforcing the idea that much of the system’s usage is work-related.

Looking at trips over time, and excluding July (when the system had just launched), **trip counts increase from August through October**, then **decline in November and December**, which coincides with colder weather. This suggests that **bikeshare usage is weather-dependent**, but to confirm this hypothesis, external weather data (e.g., temperature, precipitation, wind) would be needed to formally test the relationship.


**Multivariate Exploration:**
When trips are broken down by **user type (customer vs. subscriber)**, clearer behavioral patterns emerge. **Customers** (casual riders) tend to ride more on **weekends** and during the summer months, and their trips are more common around **tourist-heavy areas** such as the Ferry Building and the Embarcadero.

**Subscribers**, in contrast, show a strong **weekday** pattern consistent with commuting. Their trip counts increase steadily after the system launch and then decline as the weather gets colder, matching the seasonal trend seen earlier.

In terms of trip length, **customers generally ride longer than subscribers**, which aligns with recreation/leisure use versus routine commuting. Interestingly, both groups show **longer trip durations at night and in December**. This could be related to the holiday season (more leisure riding, fewer time constraints), but the nighttime pattern in particular would need additional data (e.g., weather, event schedules, or weekend/weekday split at night) to confirm the cause.


## Key Insights for Presentation  
Most trips are concentrated in **San Francisco** and are well integrated with **public transit hubs** such as Caltrain, BART, and the Ferry terminals. This suggests that the bikeshare system is being used as a **first-/last-mile connector.**

**User type** is a key factor in explaining when and where trips occur. **Customers** ride more on **weekends** and in **August*8, and their trips tend to be **longer**, consistent with leisure or tourist behavior. **Subscribers**, on the other hand, ride more on **weekdays**, showing a commute-oriented pattern, and their trip counts decline as the weather becomes colder (i.e., they are sensitive to seasonal/climatic conditions rather than “climate change”).

Because these two groups behave differently across **time, location, and trip duration**, future analyses should model **customers and subscribers separately** and, if possible, enrich the dataset with external variables (e.g., weather, events, transit schedules) to improve explanations and predictions.


## Review
* [Udacity Review 1](https://github.com/jemc36/Udacity-DAND-DataVisualization-Ford-GoBike/blob/master/Udacity%20Reviews%201.pdf)  
* [Udacity Review 2](https://github.com/jemc36/Udacity-DAND-DataVisualization-Ford-GoBike/blob/master/Udacity%20Reviews%202.pdf)   
