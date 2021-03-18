# Coding Assignment
In this assignment, you will be building a small Angular application that displays a filterable list of characters from the movie franchise Star Wars. You will be querying data from an open API called [SWAPI (Star Wars API)](https://swapi.co/) that should give you access to all data that is needed to complete the assignment. If you are not familiar with Star Wars, don't worry, prior knowledge of the movies is not required to complete the assignment. 

## App Overview
The app will consist of a main view that will display the list of characters and a filter section, where the user can filter the characters by certain criteria. Clicking on one of the characters from the list will open a detail view of this character. When the user changes the filter settings in the filter section, the list of characters should instantly adapt to only show characters that match the chosen filter settings.

### Character List
The character list should be a simple list that displays the name of the character. Each list entry should be clickable and open the detail view for the selected character when the user clicks the list entry.

### Filter
The filter section should allow the user to filter the list of characters according to the following filter settings:

* The movie the character appeared in (i.e. show only characters that appeared in Episode IV: A New Hope)
* The character's species (i.e. show only characters that are human)
* A range of years that the character's birth year falls in (i.e. show only characters born between 30 BBY and 5 ABY, see API documentation for field `birth_year` at https://swapi.co/documentation#people)

All filter settings should be treated using an AND relationship, i.e. if the user chooses to filter by movie and species, only characters that appear in the given movie AND are of the specified species should be displayed.

### Character Details
The character details that are shown when the user selects a character from the character list should show a brief summary of the character, including the name of the character, the movie the character appeared in, the species of the character and the spaceships associated with the character. For instance for the character "Han Solo", the detail view should display the following information:

> **Name:** Han Solo  
> **Species:** Human  
> **Movies:** Episode IV, Episode V, Episode VI, Episode VII  
> **Spaceships:** Millenium Falcon, Imperial shuttle  

Feel free to come up with your own design for this view!

## Further Details

### Project Setup
Please use the Angular CLI to set up the application. We should be able to start the application using the `npm start` command. The app should use the latest version of Angular (11 at the time of writing).

### SWAPI
The [Star Wars API](https://swapi.co/) should be used to complete this assignment. The most important endpoint will be the `/people` endpoint to query the characters to display in the character list (see https://swapi.co/documentation#people). As the SWAPI does not support filtering the data, it will be necessary to fetch all data and filter on the client side. Make sure not to send unneccessary API requests.

### Character Details
The character details view should make use of the Angular Router, i.e. each character should be directly reachable through a unique URL, such as `/characters/5` for the character with the ID 5.

### Reactive Patterns
It is highly reccomended to make use of reactive patterns (Observables, including observable operators) to complete this assignment. Additionally, you should use [*reactive forms*](https://angular.io/guide/reactive-forms) for the filter settings.

### External Libraries
You are allowed to use any external library to complete this assignment. You are also allowed to use UI libraries like Bootstrap or Angular Material. Just make sure that the final app looks decent and consistent.
