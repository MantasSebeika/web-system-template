# Pokemon DATABASE

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
- [ ] Gets all pokemon by id.
    - Returns 200 (OK) list of all Pokemons.
    - Returns 200 with empty list if no pokemon found.
    - Returns 404 (NotFound) if Pokemon doesn't exist.
- Get a pokemon by its name. Method: Get, /api/pokemon/:name
- [ ] Gets all pokemon by name.
    - Returns 200 (OK) list of all Pokemons.
    - Returns 200 with empty list if no pokemon found.
    - Returns 404 (NotFound) if Pokemon doesn't exist.
- Get a pokemons list by their type. Method: Get, /api/pokemon/:type
- [ ] Gets all Types.
    - Returns 200 (OK) list of all Types.
    - Returns 200 with empty list if no Types found.
    - Returns 404 (NotFound) if Type doesn't exist.
- Get a pokemons list by their size. Method: Get, /api/pokemon/:size
- [ ] Gets all Pokemon by size.
    - Returns 200 (OK) list of all Pokemons by size.
    - Returns 200 with empty list if no Size found.
    - Returns 404 (NotFound) if Size doesn't exist.
- Get a pokemons list by their weight. Method: Get, /api/pokemon/:weight
- [ ] Gets all Pokemon by weight.
    - Returns 200 (OK) list of all Pokemons by weight.
    - Returns 200 with empty list if no weight found.
    - Returns 404 (NotFound) if weight doesn't exist.
- Delete a pokemon. Method: Delete, /api/pokemon/:id
- [ ] Deletes Pokemon by id.
     - 200 deleted
     - 404 not found
- Update a pokemon. Method: Update, /api/pokemon/:id
    - [ ] Updates Pokemon by id.
     - 200 updated
     - 404 not found
- Post a new pokemon. Method: Post, /api/pokemon/
- [ ] Creates new Pokemon.
    - 502 (Bad Gateway) if given Pokemon was invalid.
    - 202 if Pokemon posted.
    - 500 if some internal errors occured.

## UI
It will be just three windows. Main - where you can get list of pokemons by filter or search. Second - You can look at one pokemon stats, change them or delete pokemon. Third - Add new pokemon. 

- Main:
  - A list of all pokemon: ID, Name, Type, Type2, size, weight. 
  - Possible actions: 
    - New: opens Third window (Create a new pokemon mode)
    - Filter: Filters the list by selected ID, type, name, size, weight
    - Edit: Opens second window with the pokemon (Edit mode)
    - Delete: Opens second window where you can Delete the pokemon

- Second:
  - A single pokemons data
  - Possible actions:
    - Delete: Deletes the pokemon and opens the Main window
    - Cancel: Does not save the changes and opens Main window
    - Save: Save made changes
    
- Third:
  - A single pokemons data
  - Possible actions:
    - Cancel: Does not save the changes and opens Main window
    - Save: Saves new pokemon

https://wireframe.cc/9S5Ood
