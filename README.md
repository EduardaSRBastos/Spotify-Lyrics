# Spotify Lyrics

This simple web application displays the currently playing track from Spotify and fetches its lyrics using the Vagalume API.

## Usage

1. Clone the repository to your local machine.
2. Create a `config.json` file in the root directory of the project with the following structure:

    ```json
    {
        "clientId": "YOUR_SPOTIFY_CLIENT_ID",
        "apiKey": "YOUR_VAGALUME_API_KEY"
    }
    ```

    Replace `YOUR_SPOTIFY_CLIENT_ID` with your Spotify client ID and `YOUR_VAGALUME_API_KEY` with your Vagalume API key.

3. **Web Version**:
   - Run and open `index.html` in your web browser.

4. **Electron Version**:
   - Ensure you have Node.js and npm installed on your machine.
   - Install Electron by running `npm install electron --save-dev`.
   - Run `npm install` to install dependencies.
   - Run `npm start` to start the Electron application.
   - Alternatively, to open the app by clicking on an executable file, run `npx electron-packager . Spotify-Lyrics`.

## How it Works

- When the page loads, it fetches the currently playing track from Spotify using the Spotify Web API.
- It then fetches the lyrics of the currently playing track using the Vagalume API.
- The lyrics are displayed on the webpage.

## Dependencies

- jQuery: Used for making AJAX requests to the Vagalume API.
- Spotify Web API: Used for fetching the currently playing track from Spotify.
- Vagalume API: Used for fetching the lyrics of the currently playing track.
- Electron: Used for creating standalone desktop applications.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.