# atstation

atstation is a lightweight, client-side web app that shows the next train departure based on your current location and time of day. It uses the HTML5 Geolocation API to detect your nearest station and then selects the appropriate schedule for AM (outbound) or PM (return) trips. Customize the station list and timetable data to match your own train lines.

!(ss)[ss.png]

## Quick Start
1. Download or clone the repository and open `index.html` in your browser.  
2. Allow location access when prompted to enable nearest-station detection.  
3. View live countdowns to your next departure.

## Configuration
At the top of the `<script>` in `index.html`, update the following to suit your trains:
- **stationNames**: an ordered array of your station IDs (e.g., `["A","B","C"]`).  
- **stationCoords**: map each ID to its `{ lat, lon }` coordinates.  
- **timetables**: define `AM`/`PM` schedules with keys like `"s1_s2"` and arrays of `"HH:MM"` strings.

Only these three sections need editing—no other code changes required.

## Features
- **Geolocation-based**: Automatically finds your nearest station via the Geolocation API.  
- **Time-of-day routing**: Uses forward routes before noon, return routes after.  
- **Next two departures**: Shows minutes until the next two trains.  
- **Auto-refresh**: Updates every minute to keep countdowns accurate.  

Note: The geolocation is not automatically updated; you must reload the page to get a new location.

## Credit
atstation program is licensed under MIT License.  
Contact: X @aike1000
