# 👩‍💻 Developer Manual: AirAware

This document is for future developers who wish to maintain or expand the AirAware application.

---

## 🚀 Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/airaware.git
cd airaware

2. Install Dependencies
bash
Copy
Edit
npm install
3. Set Up Environment Variables
Create a .env file in the root of the project and add the following line with your OpenWeather API key:

env
Copy
Edit
REACT_APP_WEATHER_API_KEY=your_api_key_here
▶️ Running the Application Locally
To start the development server:

bash
Copy
Edit
npm start
This will run the app on http://localhost:3000

🧪 Running Tests
We use manual API testing with Insomnia (see /docs/api-testing.pdf), but you can begin automating testing by adding:

bash
Copy
Edit
npm test
Note: Test files can be added using Jest or Vitest for front-end testing if future expansion is planned.

🌐 Server API Endpoints
These custom endpoints are located in the server/api/ directory and connect to the Supabase backend.

1. GET /api/user-cities
Retrieves the list of saved cities associated with the current user from Supabase.

2. POST /api/add-city
Adds a new user-specified city to their list of favorites in the database.

Both of these endpoints are called by the front end using fetch() and integrated into the user interface.

📡 External APIs Used
API Name	Purpose
OpenWeather Geocoding API	Converts user-inputted city names to latitude and longitude
OpenWeather Air Pollution API	Provides real-time AQI and pollutant data (CO, NO2, O3, PM2.5, etc.)
Browser Geolocation API	Retrieves the user's location directly from the browser

🧱 Known Bugs / Limitations
API rate limits may cause temporary issues when too many requests are made.

Geolocation may be blocked by user permissions or fail in Safari Private Mode.

Supabase write operations may be delayed depending on internet speed and tier.

📈 Roadmap for Future Development
Add user authentication using Supabase Auth or Firebase

Let users set daily or weekly air quality alerts

Include health recommendations based on AQI score

Implement dark mode toggle

Add test coverage for custom APIs using Jest/Supertest

