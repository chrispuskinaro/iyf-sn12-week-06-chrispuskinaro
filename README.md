
# Week 06 - Lesson 12: Working with APIs - Weather Dashboard

**Student:** Chrispus Kinaro  
**Season:** Season-12 | IYF Weekend Academy  
**Live Demo:** [Add your GitHub Pages link here after deploy]

## Project Overview
Weather dashboard using OpenWeatherMap API. This project feeds CommunityHub frontend pattern - the fetch + loading/error pattern used here is exactly how CommunityHub loads data.

## What I Learned (Lesson 12 Objectives)
- **Explain REST API basics:** REST uses HTTP methods (GET) to request resources via URL endpoints, returns JSON
- **Fetch external data and render it in the DOM:** Used `fetch()` with async/await to get weather data and inject to HTML
- **Handle loading and error states:** Shows "Loading..." while fetching, shows error message if city not found or API fails

## Hands-On Activities Completed
1. ✅ Fetch data from a public API - OpenWeatherMap `https://api.openweathermap.org/data/2.5/weather`
2. ✅ Display data in the DOM - City, temp, description, humidity, wind
3. ✅ Handle loading and error states - try/catch with loading indicator
4. ✅ Build search/filter functionality - Search by any city name

## Tech Stack
- HTML5, CSS3, JavaScript (ES6+)
- Fetch API + async/await + Promise handling (from Lesson 11)
- GitHub Pages + GitHub Actions

## How to Run Locally
1. Clone: `git clone https://github.com/Chacha-A-Chacha/iyf-sn12-week-06-chrispuskinaro.git`
2. Create `config.js` in root: `const API_KEY = "YOUR_OPENWEATHER_KEY";`
3. Open `index.html` with Live Server

## Security
`config.js` is in `.gitignore`. For deployment, API key is stored as GitHub Secret `OPENWEATHER_API_KEY` and created by `.github/workflows/deploy.yml`:
```yaml
echo "const API_KEY = '${{ secrets.OPENWEATHER_API_KEY }}';" > config.js
