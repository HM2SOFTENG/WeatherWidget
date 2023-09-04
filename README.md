
# Weather Display Component

The `WeatherDisplay` component is a part of a React application designed to showcase weather information. It allows users to view weather details for their current location or search for weather information by location name or zip code. The component utilizes the OpenWeatherMap API through the `weatherService` to fetch and display weather data.

## Usage

To integrate the `WeatherDisplay` component into your React application, follow these steps:

1. **Installation**: Ensure you have Node.js and npm (Node Package Manager) installed on your system. If not, you can download and install them from [https://nodejs.org/](https://nodejs.org/).

2. **Installation of Dependencies**: If not already done, navigate to your project directory and run the following command to install the necessary dependencies:

   ```sh
   npm install
Weather Service Configuration: Configure the weatherService to interact with the OpenWeatherMap API and provide the required API key.

Implementation: Use the WeatherDisplay component in your application. Import it and include it within your desired component's JSX.

jsx
Copy code
import React from "react";
import WeatherDisplay from "./WeatherDisplay"; // Update the path to the WeatherDisplay component

function App() {
  return (
    <div className="App">
      <WeatherDisplay />
    </div>
  );
}

export default App;
Features
The WeatherDisplay component provides the following features:

Display weather information for the user's current location if geolocation is available.
Allow users to search for weather information by entering a city name or zip code.
Display weather data including temperature, weather conditions, wind speed, precipitation, and more.
Handle errors gracefully when geolocation is not available or when weather data cannot be retrieved.
Components
WeatherDisplayCard: A separate component responsible for rendering the weather information as a card.
State
weatherData: Manages weather-related data including city name, weather icon, conditions, temperature, wind speed, and more.
showSearchBar: Determines whether the search bar is shown based on geolocation availability.
Functions
getCurrentPositionSuccess: Handles successful geolocation retrieval and fetches weather data.
getCurrentPositionError: Handles errors in geolocation retrieval.
onGetWeatherDataError: Handles errors when fetching weather data.
onGetWeatherDataSuccess: Processes fetched weather data and updates the weatherData state.
onSubmit: Handles form submission for searching weather information by location name or zip code.
Dependencies
weatherService: A service that interacts with the OpenWeatherMap API.
Formik and Form: Used for form management and validation.
Col and Row from react-bootstrap: Used for responsive layout.
weatherSchema: A validation schema for the search form.
Toastify: A library for displaying toast notifications.
Important Notes
Make sure to configure the weatherService properly with your OpenWeatherMap API key.
Update the paths to your imported components as needed.
Customize the styling and appearance of the components to match your application's design.
