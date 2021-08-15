## Overview of the Project
This project aims to collect data and improve the user interface (customer search page) of the PlanMyTrip (a travel technology company) app for the customers who look for hotels around the world and have specific weather condition preferences. 
In this project, different sources which are introduced as follows are used:
- Programming language: Python (version 3.8.8)- code is written in Jupyter Notebook.
- Dependencies: [Citypy](https://github.com/wingchen/citipy), Numpy (version 1.21.0), Pandas (version 1.3.0), Matplotlibs (version 3.4.2), gmaps (version 0.9.0), Python Requests (version 2.25.1)
- API: [Open Weather](https://openweathermap.org/api), [Google Maps and Places](https://console.cloud.google.com/google/maps-apis/new?project=prime-boulevard-321320), and [Google Directions](https://cloud.google.com/maps-platform/)

## Results
Three steps are followed to reach the goal of this project:<br>
1. Collected weather data (description) of each city:<br>
First, 2000 coordinate sets (latitude and longitude) are randomly generated to get weather data (Numpy library). Then, the closest cities to generated coordinates are determined (Citypy module) and stored in a list. Next, the information about weather (e.g., maximum temperature, cloudiness, humidity, and so on) is requested for each city from the Open Weather API. Finally, the DataFrame (Figure 1)) is created (using Pandas library) and exported ([weather_data.csv file](https://github.com/elp192/World-Weather-Analysis/blob/35511af81f7806505bc2a0aebdf25488e1849952/weather_data/weather_data.csv)).
<p img align="center" width="100%">
<img width="500" alt="weather_data_DataFrame" src="https://user-images.githubusercontent.com/85843401/129462668-e9ad7e5b-875b-48b4-9f58-d38a482cdd4f.png">
<figcaption>Figure 1: Demonstration of weather data DataFrame.</figcaption></figure/> 
<p align="center">
</p>

2. Determined travel destination map (hotel name) for each customer based on their weather preference:<br>
In this step, the preferred temperature range is asked from a traveler/customer, and the weather database is filtered accordingly. Then, the hotel information is requested from Google Maps and Places API. Finally, the [weather_search](https://github.com/elp192/World-Weather-Analysis/blob/1ec60a787f6e497426fadaa4eea5830c0282b514/vacation_search/weather_vacation.csv) DataFrame (Figure 2) is created and exported. Figure 3 represents the created map (using gmaps) with information about traveler search. 
<p img align="center" width="100%">
<img width="500" alt="vacation_search_DataFrame" src="https://user-images.githubusercontent.com/85843401/129462785-6f29701e-ba3e-40b9-be78-02b500b27bdb.png">
<figcaption>Figure 2: Demonstration of vacation search DataFrame.</figcaption></figure/> 
<p align="center">
</p>

<p img align="center" width="100%">
<img width="500" alt="weather_vacation_map" src="https://user-images.githubusercontent.com/85843401/129462919-bea716bc-3022-44b6-b77a-32689e42c5b9.png">
<figcaption>Figure 3: Demonstration of travel destination map.</figcaption></figure/> 
<p align="center">
</p>

3. Determined travel itinerary map for each customer based on selected weather conditions: <br>
In this step, the traveler chooses four hotels among the obtained locations in the previous step. Then, the route of travel is determined using Google Direction API (Figure 4).
<p img align="center" width="100%">
<img width="250" alt="travel_map_markers" src="https://user-images.githubusercontent.com/85843401/129463058-3f016baf-41e1-400d-93c3-4e323a33e2e3.png">
<img width="400" alt="travel_map_direction" src="https://user-images.githubusercontent.com/85843401/129463060-334b3967-9146-4427-b292-92cfba92d930.png"><figcaption>Figure 4: Demonstration of left) selected hotels, rigth) travel destination route.</figcaption></figure/> 
<p align="center">
</p>
