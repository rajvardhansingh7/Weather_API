# Weather App

A clean and simple web application that displays the current weather for any city. This app fetches real-time data from the OpenWeatherMap API and presents it in a minimalist, dark-mode interface.

## Preview

![Weather App Screenshot](https://github.com/rajvardhansingh7/Weather_API/blob/main/image.png)

## Features

* **City Search:** Get the current weather for any city in the world.
* **Real-time Data:** Displays the city name, current temperature in Celsius, and a weather description (e.g., "clear sky", "light rain").
* **Error Handling:** Shows a user-friendly error message if the city is not found.
* **Dark Mode UI:** A modern, clean, and responsive dark-mode design.

## Technologies Used

* **HTML5:** For the structure of the app.
* **CSS3:** For all styling and layout.
* **JavaScript (ES6+):** For app logic, API fetching (`async/await`), and DOM manipulation.
* **OpenWeatherMap API:** Used to source the live weather data.

## Setup and Configuration

To run this project locally, you need to provide your own OpenWeatherMap API key.

### 1. Get Your API Key

1.  Go to [OpenWeatherMap.org](https://openweathermap.org/) and sign up for a free account.
2.  Navigate to your account's "API keys" tab and copy your default API key.

### 2. (CRITICAL) Secure Your API Key

Your `script.js` file currently has an API key visible. **You must never push secret keys to a public GitHub repository.** Here is the best way to fix this:

1.  **Create a new file** in your project folder named `config.js`.
2.  **Inside `config.js`**, add your API key like this:
    ```javascript
    const API_KEY = "YOUR_API_KEY_HERE";
    ```
3.  **In `index.html`**, add a script tag to load this new file *before* your main `script.js` file. Your file should look like this:
    ```html
    <script src="config.js"></script>
      <script src="script.js"></script>
    </body>
    </html>
    ```
4.  **In `script.js`**, **DELETE** the line:
    ```javascript
    const API_KEY = "5f56d525d1619d0a2cd2eac4ce55588e"; //env variables
    ```
    (Your app will now get the `API_KEY` variable from `config.js`, which is loaded first).

5.  **Create a new file** in your project folder named `.gitignore`.
6.  **Inside `.gitignore`**, add the following line. This tells Git to *never* upload `config.js`, keeping your key safe.
    ```
    config.js
    ```

### 3. Run the App

After completing the configuration, just open the `index.html` file in your web browser!
