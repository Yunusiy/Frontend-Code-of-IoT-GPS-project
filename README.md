# GPS Dashboard

This project is a web-based dashboard for tracking and displaying real-time GPS data using an ESP32. The GPS data includes longitude, latitude, speed, altitude, direction, and more. The dashboard uses Firebase for data storage and Mapbox for map visualization.
![image](https://github.com/Yunusiy/Frontend-Code-of-IoT-GPS-project/assets/89139698/a6551632-4c7c-40d5-9699-3186aa30e251)

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Technologies Used](#technologies-used)
- [File Structure](#file-structure)
- [License](#license)

## Features

- **Real-time Data Streaming:** Display live GPS data from the ESP32.
- **Map Visualization:** View GPS coordinates on a Mapbox map.
- **Distance Calculation:** Calculate the distance from the current location to a specified point.
- **Data Reset:** Reset the displayed data.
- **Scroll Control:** Scroll to top and bottom of the page with ease.

## Installation

1. **Clone the Repository:**
   ```sh
   git clone https://github.com/yourusername/gps-dashboard.git
   cd gps-dashboard
   ```

2. **Set Up Firebase:**
   - Create a Firebase project and obtain your Firebase configuration.
   - Replace the Firebase configuration in `js/script.js` with your own.

3. **Install Dependencies:**
   This project uses Bootstrap, Mapbox, and Firebase. These are included via CDN in the HTML file.

4. **Run the Project:**
   Open the `index.html` file in your browser.

## Usage

1. **Start the ESP32:**
   Ensure your ESP32 is running the GPS tracking code and is connected to Firebase.

2. **Open the Dashboard:**
   Open `index.html` in your browser to view the real-time GPS data.

3. **Interact with the Dashboard:**
   - View live data updates in the sidebar.
   - See the current location on the map.
   - Click the "How Far from me?" button to calculate the distance from your current location.
   - Use the reset button to clear all displayed data.

## Configuration

### Firebase Configuration

Update the Firebase configuration in `js/script.js`:
```javascript
var firebaseConfig = {
  apiKey: "your_api_key",
  authDomain: "your_project_id.firebaseapp.com",
  databaseURL: "https://your_project_id.firebaseio.com",
  projectId: "your_project_id",
  storageBucket: "your_project_id.appspot.com",
  messagingSenderId: "your_messaging_sender_id",
  appId: "your_app_id"
};
firebase.initializeApp(firebaseConfig);
```

### Mapbox Configuration

Update the Mapbox access token in `js/script.js`:
```javascript
mapboxgl.accessToken = 'your_mapbox_access_token';
```

## Technologies Used

- **HTML5**: Structure of the dashboard.
- **CSS3**: Styling and layout (including Bootstrap for responsiveness).
- **JavaScript**: Functionality and Firebase integration.
- **Firebase**: Realtime database for storing GPS data.
- **Mapbox GL JS**: Map visualization.

## File Structure

```
gps-dashboard/
├── static/
│   ├── css/
│   │   └── style.css       # Custom CSS styles
│   ├── images/
│   │   ├── hut.png         # Image for start point marker
│   │   ├── reset-data.png  # Image for reset button
│   │   ├── go-to-top.png   # Image for scroll to top button
│   │   └── go-to-bottom.png# Image for scroll to bottom button
│   └── js/
│       └── script.js       # JavaScript for Firebase and Mapbox integration
└── index.html              # Main HTML file
```



Feel free to contribute, open issues, or create pull requests. Enjoy using the GPS Dashboard!
