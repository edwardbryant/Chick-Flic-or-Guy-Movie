# Chick Flic or Guy Movie?

A web app that attempts to settle the argument of whether a given movie is a "chick flic" or a "guy movie" (appropriately named, don't you think?). The original version of the app was done as an assignment for Thinkful.com. As stated on the app itself, "Chick Flick or Guy Movie uses HTML, CSS, JS & jQuery combined with the power of sexist clichés to guess at whether a movie was targeted at a female or male audience. Specifically, it combs through the title and description of the movie to find certain keywords (e.g., "romantic" or "war")."  

# Design

The design of the web app was based on old boxing posters. 

# Movie Query

The app lets users enter the name of a movie to determine if it is a chick flic or a guy movie. The app takes the user input and attempts to match it against a movie title using the API at TheMovieDB.org. Rather than present the user with a number of possible matches, for simplicity sake the app simply assumes the closet match is the correct match. As a consequence, some movie titles must be entered exactly ("Transformers" vs "Transformers Dark of the Moon"), while some instances in which multiple movies share the same exact title will prevent anything other than the first match from returning (see issues below)   

# Random Movie Query

As an alternative to entering a movie title, the app allows users to let the app pick a "random" movie. This feature works utilizing the popular movie listing API at TheMovieDB.org. The script selects a random page from the lists first 5 pages and selects a random title of the 20 available titles on that page. Taken together, this selects one of the current top 100 most popular titles according to the API service. Although not truely random, this allows for a random selection with which the user is likely to be familiar.    

# Issues

- user-entered title option doesn't allow for movie title matching in instances of multiple movies with same exact title, if the desired movie is not the first ranked match.
- the app is predictably unreliable for movies that have little or no summary information available through the API service (a situation most common for movies yet to be released). 
