# Spotify Lyrics

This simple web application displays the currently playing track from Spotify and fetches its lyrics using the Vagalume API.

</br>

## Table of Contents

- [Usage](#usage)
  - [Credentials](#credentials)
  - [Web Version](#web-version)
  - [Electron Version](#electron-version)
- [How it Works](#how-it-works)
- [Dependencies](#dependencies)
- [License](#license)

</br>

## Usage

#### Credentials
1. Get your Spotify Client ID and Secret from [Spotify Developer](https://developer.spotify.com/dashboard/).
   1. Click in 'Create App' and add a 'Name' and 'Description'.
   2. Add http://localhost:8080/index.html in 'Redirect URIs'.
   3. Click in the checkbox that you accept the Spotify's Developer ToS and click in 'Save'.
   4. Go to Settings inside of the app that you just created, and you have your Client ID.
2. Get your Vagalume API Key from [Vagalume](https://www.vagalume.com.br).
   1. Go to 'Meus Dados' on your profile and click in 'API'.
   2. Click in 'Adicionar Crendencial' and add a 'Nome'.
   3. The 'Crendencial' is your API Key.
3. Clone the repository to your local machine.
4.  Create a `config.json` file in the root directory of the project with the following structure:

    ```json
    {
        "clientId": "YOUR_SPOTIFY_CLIENT_ID",
        "apiKey": "YOUR_VAGALUME_API_KEY"
    }
    ```

    Replace `YOUR_SPOTIFY_CLIENT_ID` with your Spotify client ID and `YOUR_VAGALUME_API_KEY` with your Vagalume API Key.

</br>

#### Web Version:
   - Run and open `index.html` in your web browser.

#### Electron Version:
   - Ensure you have Node.js and npm installed on your machine.
   - Install Electron by running `npm install electron --save-dev`.
   - Run `npm install` to install dependencies.
   - To use the application with a local server:
     1. Install a simple HTTP server globally by running `npm install -g http-server`.
     2. Navigate to the project directory and run `http-server`.
   - Run `npm start` in other terminal in the project directory to start the application.
   - Alternatively, to open the app by clicking on an executable file, run `npx electron-packager . Spotify-Lyrics`.
     1. The packaged application will be available in the `Spotify-Lyrics` directory.

</br>

## How it Works

- When the page loads, it fetches the currently playing track from Spotify using the Spotify Web API.
- It then fetches the lyrics of the currently playing track using the Vagalume API.
- The lyrics are displayed on the webpage.
- If the music changes, you will need to reload the page.

</br>

## Dependencies

- jQuery: Used for making AJAX requests to the Vagalume API.
- Spotify Web API: Used for fetching the currently playing track from Spotify.
- Vagalume API: Used for fetching the lyrics of the currently playing track.
- Electron: Used for creating standalone desktop applications.

</br>

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
