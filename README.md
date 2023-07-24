# Track My Music

![My Spotify Logo](https://st.depositphotos.com/37050820/58882/v/450/depositphotos_588825950-stock-illustration-spotify-logo-dark-mode.jpg)

Welcome to the Track My Music project! 

Everyday we listen to hundreds and thousands of songs but have you ever thought about tracking your listening habits? If yes, then I believe this project will be a very helpful start for you. This project aims to help you track your listening habits of Spotify using your own streaming history and liked songs. It also utilizes the Spotify API to pull data about different genres associated with different artists. The processed data is then used to create an interactive Tableau dashboard, providing insights into your music preferences and habits.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [How to request Spotify Data](#how-to-request-spotify-data)
- [How to use Spotify API](#how-to-use-spotify-api)
- [Data Collection and Preprocessing](#data-collection-and-preprocessing)
- [Tableau Dashboard](#tableau-dashboard)
- [Contributing](#contributing)

## Introduction
In the age of digital music streaming services like Spotify and Prime Music, music lovers often find themselves curious about their listening habits and music preferences. The Track My Music project was created to cater to this curiosity by enabling users to gain insights into their Spotify listening habits, favorite tracks, and the genres they tend to enjoy the most.

## Features
- **Listening Habit Tracking:** By utilizing your own Spotify streaming history and liked songs data, the project enables you to track your listening habits over time.

- **Genre Analysis:** The Spotify API is leveraged to retrieve data on genres associated with different artists. This helps in understanding the diversity of genres you enjoy.

- **Tableau Dashboard:** The processed data is visualized using Tableau, providing an interactive dashboard that showcases various statistics and insights about your music preferences.

## Installation
To run the My Spotify project locally: 

Clone the repository:
```
git clone https://github.com/riabhatnagar0610/My-Spotify-Project.git
```


## How to request Spotify Data
Access your Spotify account dashboard at [Spotify Dashboard](https://www.spotify.com/). In the privacy settings, you’ll find the option to request your data. This requires some patience. Spotify says it takes up to thirty days, but it’s usually much faster.
Eventually you will get an email with your Spotify data in a .zip file. Extract the MyData folder and copy it in your working folder.

## How to use Spotify API
To use the API, ensure you have a Spotify account (free or premium, doesn't matter) and follow the below steps : 

Obtain Spotify API credentials:
   - Go to the Spotify Developer Dashboard (https://developer.spotify.com/dashboard/).
   - Log in with your Spotify account or create one if needed.
   - Create a new app and go to the settings of your app to obtain your Client ID and Client Secret.

## Data Collection and Preprocessing
MyData folder will contain streaming history and your library files in the .json format. Refer to the `my-spotify-project(1).ipynb` file in the directory for the full code.

- Import the required Python libraries
  
  ![image](https://github.com/riabhatnagar0610/My-Spotify/assets/91281889/e225270e-38ff-4854-bce5-9dd281686cf9)

- Merging files to obtain a combined data frame for ease of usability
  
  ![image](https://github.com/riabhatnagar0610/My-Spotify/assets/91281889/41f1a3c3-1fa5-46c3-a333-3c7b9e433978)

- A quick note: Please remember to clean your YourLibrary.json file so that it only contains the tracks row bounded by square brackets []. Otherwise it will throw an error saying the rows must be of equal length for it to be converted to a data frame.

 ![image](https://github.com/riabhatnagar0610/My-Spotify/assets/91281889/28853544-a26b-4601-9945-b8063e55a25b)

- Now, let's find out if your streamed tracks are actually present in your liked songs or not

  ![image](https://github.com/riabhatnagar0610/My-Spotify/assets/91281889/aa747120-9036-49bb-a95b-6355a7bb73e3)

- Yay! All the data cleaning and processing is done. Now it's time for the exciting part - working with the Spotify API

  ![image](https://github.com/riabhatnagar0610/My-Spotify/assets/91281889/32050f35-f59c-4384-b906-0d0591b7ef06)

  ![image](https://github.com/riabhatnagar0610/My-Spotify/assets/91281889/5d1835ab-d841-47cd-af46-1ceb0c5bf8f5)

  ![image](https://github.com/riabhatnagar0610/My-Spotify/assets/91281889/b74884c2-c70e-4cf1-9d63-60e5ac98db70)

- Create a blank dictionary for obtaining genre data through track and artist URIs

  ![image](https://github.com/riabhatnagar0610/My-Spotify/assets/91281889/e095d7b5-f2d9-42d6-8479-74917bceae84)

- Convert the dictionary to data frame and expand on genres. Lastly, save the processed files as csv

  ![image](https://github.com/riabhatnagar0610/My-Spotify/assets/91281889/8aed83a1-563d-4793-91fb-1b93d63d3d12)

  ![image](https://github.com/riabhatnagar0610/My-Spotify/assets/91281889/71071419-fc0b-4fe7-b577-1b9233177eaa)


## Tableau Dashboard
The Tableau dashboard presents the processed data in an interactive and visually appealing manner. It includes charts, graphs, and filters to help you explore and understand your music preferences.
My tableau dashboards can be found at [Spotify Dashboards](https://public.tableau.com/app/profile/ria.bhatnagar)

## Contributing
Contributions to the project are welcome! If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.
We hope you enjoy using the Track My Music project and gain valuable insights into your music listening habits! If you have any questions or need assistance, don't hesitate to reach out. Happy listening!
