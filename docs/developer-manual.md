# 👩‍💻 Developer Manual: AirAware

This document is for future developers who wish to maintain or expand the AirAware application.

---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/airaware.git
cd airaware

2. Install Dependencies
npm install

3. Set Up Environment Variables
Create a .env file in the root of the project and add the following line with your OpenWeather API key:
REACT_APP_WEATHER_API_KEY=your_api_key_here

4. Running the Application Locally
To start the development server:
npm start
This will run the app on http://localhost:3000

5. Running Tests
You can begin automating testing by adding:
npm test

6. Server API Endpoints
These custom endpoints are in the server/api/ directory and connect to the Supabase backend.

a.) GET /api/user-cities
Retrieves the list of saved cities associated with the current user from Supabase.

b.)  POST /api/add-city
Adds a new user-specified city to their list of favorites in the database.

Both endpoints are called by the front end using fetch() and integrated into the user interface.

External APIs Used
API Name	Purpose
OpenWeather Geocoding API	converts user-inputted city names to latitude and longitude
OpenWeather Air Pollution API	provides real-time AQI and pollutant data (CO, NO2, O3, PM2.5, etc.)
Browser Geolocation API	  retrieves the user's location directly from the browser

Known Bugs / Limitations
- API rate limits may cause temporary issues when too many requests are made.

- Supabase write operations may be delayed depending on internet speed and tier.

Roadmap for Future Development
- Let users set daily or weekly air quality alerts

- Include health recommendations based on AQI score

- Add test coverage for custom APIs 
