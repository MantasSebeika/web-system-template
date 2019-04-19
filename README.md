# POkemon DATABASE

## Description
- [ ] Web database about all pokemons statistics that they have. Also if new generation comes out or status get changed you can add new pokemon, delete it or change pokemon status.

## Pokemon
Atributes:
- ID : Pokemon ID, mandatory (number, 0<ID<999)
- Name : Pokemon name, mandatory (String, <25 char)
- Type : Pokemon type, mandatory (Array, size = 15)
- Type2 : Pokemon secondary type (Array, size = 15)
- Ability : Pokemon special abillity (String, <80 char)
- Size : Pokemon size in cm (number, 0<Size<90000)
- Weight : Pokemon weight in kg (number, 0<Weight<50000)
- Description : Pokemon description (String, <120)

## API
Possibilities:
- Get a pokemon by its ID. Method: Get, /api/pokemon/:id
- Get a pokemon by its name. Method: Get, /api/pokemon/:name
- Get a pokemons list by their type. Method: Get, /api/pokemon/:type
- Get a pokemons list by their size. Method: Get, /api/pokemon/:size
- Get a pokemons list by their weight. Method: Get, /api/pokemon/:weight
- Delete a pokemon. Method: Delete, /api/pokemon/:id
- Edit a pokemon. Method: Put, /api/pokemon/:id
- Create a new pokemon. Method: Post, /api/pokemon/

## UI
It will be just three windows. Main - where you can get list of pokemons by filter or search. Second - You can look at one pokemon stats, change them or delete pokemon. Third - Add new pokemon. 

- Main:
  - A list of all pokemon: ID, Name, Type, Type2, size, weight. 
  - Possible actions: 
    - New: opens Third window (Create a new pokemon mode)
    - Find: Opens pokemon second window (Edit mode) if the ID is found (from the text box)
    - Filter: Filters the list by selected ID, type, name, size, weight
    - Edit: Opens second window with the pokemon (Edit mode)
    - Delete: Opens second window where you can Delete the pokemon

- Second:
  - A single pokemons data
  - Possible actions:
    - Delete: Deletes the pokemon and opens the Main window
    - Cancel: Does not save the changes and opens Main window
    - Edit: is named depending on the window mode (Edit, Create). Saves the changes on the pokemon and opens the Main window
    
- Third:
  - A single pokemons data
  - Possible actions:
    - New: Creates a new pokemon with all fields empty (except ID) and shows it in the window (Create mode)
    - Cancel: Does not save the changes and opens Main window
    - Save: Saves new pokemon
