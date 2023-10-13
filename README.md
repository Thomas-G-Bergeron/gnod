# gnod


1.Removed Features

- Time signature : is a musical notation that indicates the number of beats in each musical measure and the type of note that receives a regular pulse.
Time signature is not specific to a genra or most type of music. As it doesn't allow to discriminate between most of the songs which to remove it

- Tempo : the speed, the pulse.
Songs from the same genra may have completely different pulses, the pulse is not the most relevant criteria to define a song in our mind and we chose to remove it.

- Loudness : Represents the sound intensity of a song in decibels (dB). A higher value indicates a louder song.
Loudness is about the mixing, it doesn't change the nature or genra of the music and is therefore not relevant criteria for a cluster.

- Key : Indicates the main key of the song.
The key indicates only how high or deep the music is played, but changing the key doesn't change the music. It is therefore not a criteria to discriminate between songs


- Mode : Indicates whether the song is in major mode (1) or minor mode (0).
As the mode may only have two values and is not specific to any genra we chose not to keep this column because it gives too few informations on the music

- Liveness : Indicates the probability that a song was recorded during a live concert rather than in a studio.
Liveness of the songs doesn't impact the nature of the song, we therefore chose not to keep this criteria


2.The notebooks
There are five different notebooks:
Web_scrapping : in this notebook we scrapp the bilboard 100 webpage to build a database of the 100 most popular songs of the moment
building databases: in this notebook we clean the database of the 100 most popular songs and select a sample of the million song dataset that we downloaded from the web
id and audio features: in this notebook we use the spotify api to get the ids and audio features of every song in both databases
dimensionality reduction : in this notebook we use the three dimensionality reduction techniques and select TSNE as the most satisfactory one
cluster: in this notebook we cluster the data using three different methods and add the satisfactory clustering as columns of our main database
final function : in this notebook we build a function enabling to get recommendations of similar songs for a song inputed by the user

3.The functions
search_song(title, artist, limit): for given music title, artist and limit, the function uses the spotify api and returns a list of song ids equal to the limit
get_audio_features: for a given list of ideas, the function uses the spotify api and returns a dataframe containing corresponding audio features
add_audio_features: for two given dataframes of equal length containing both a column named 'id' the function performs a merge 
Vynila: for a given song title and artist, the function returns five song recommendations to the user

4.The presentation

We have imagined a plateform dedicated for 55-64 aged users : Vilyla, a user-firendly plateform for music lovers.
Indeed, these users do not take advantage of streaming platforms because several things push them away: creating an account, paying to listen to music, they don't want an app, and the plateforms like Spotify are too cluttered.
Vinyla is a very simple interface where you can enter the title of a song you like, and get a personalized playlist to discover new artists.






