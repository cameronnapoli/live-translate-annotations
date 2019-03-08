# Live Translate Annotations

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Using Google Cloud APIs, live translate audio into either subtitles or translated audio.

![Picture of app](translation.png)

## Speech Processing Server

Server written in Node.js. Collects, audio fragments, translates them, and upon a response from Google Cloud, responds with text from audio and translated text.

## Interface

Interface written using React.js and uses react-select library.

## Installation

To install the backend, cd into `speech_processing` directory and run `npm install` to install dependencies. To run backend server, run the following command in the same folder and then open http://localhost:8000 to make sure server is running:

    node app.js

To install and run the frontend on port 3000, run the following commands:

    cd interface
    npm install
    npm start

#### Google Cloud dependencies

For Google Cloud to connect to your account credentials, an environment variable must be set to point to a JSON file with your credentials.

To create the file and set the environment key:

*  First create JSON service account key file following the instructions [here](https://support.google.com/a/answer/7378726?hl=en).
*  Then, following the steps on the [Google quickstart page](https://cloud.google.com/speech-to-text/docs/quickstart-client-libraries?authuser=1) set the environment variable `GOOGLE_APPLICATION_CREDENTIALS` to the path to your JSON file.

For example on Unix:
```export GOOGLE_APPLICATION_CREDENTIALS=/path/to/creds.json```


#### Running the Server

To start server on port 8000, run `node app.js`.


## Dependencies
    socket.io
    @google-cloud/speech
    @google-cloud/translate
