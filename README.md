<div>
  <h1 align="center">
<!-- <img style="width: 100px" src="https://www.sendx.io/hubfs/SendPost_August2021/images/SendX-By-Logo.svg" width="100" /> -->
<br>Components
</h1>
</div>

# PokemonCard
The `PokemonCard` component is a reusable React component designed to display a Pokemon card with a link. It is implemented using the Next.js framework and incorporates the `Link` component from Next.js for seamless client-side navigation. The component takes a `name` prop, representing the name of the Pokemon, and dynamically generates a link based on that name.

## Usage

Import the PokemonCard component into your React file and include it in your JSX. Pass the name prop with the desired Pokemon name as a string.

```jsx
import { PokemonCard } from 'path-to-PokemonCard';

// Example usage:

<PokemonCard name="pikachu" />

```

## Props

### `name` (`String`, *required*)
The name of the Pokemon to be displayed on the card. Should be passed as a string.


# PokemonGrid
The `PokemonGrid` component is a React component designed to display a grid of Pokemon cards with a search functionality. It takes a list of Pokemon as a prop and allows users to search for specific Pokemon by name.

## Usage

```jsx
import { PokemonGrid } from "./path-to-PokemonGrid";

// Example usage:

<PokemonGrid pokemonList={data} />
```

## Props
### `pokemonList` ( `Array` *required*) 
An array of Pokemon objects to be displayed in the grid. Each Pokemon object should have a name property.

## State
The component utilizes the `useState` hook to manage the search functionality. It keeps track of the search text entered by the user.

## Filtering
The searchFilter function filters the list of Pokemon based on the entered search text. It performs a case-insensitive match against the Pokemon names.

# PokemonImage
The `PokemonImage` component is a React component designed to display a Pokemon image using the Next.js `Image` component. It takes the `image` and `name` props to render the image of a Pokemon.

## Props
### `image` (`String`, *required*) 
A string representing the path or URL to the image of the Pokemon.
### `name` (`String`, *required*)
A string representing the name of the Pokemon. Used for the image's alt text.



<div>
  <h1 align="center">
<!-- <img style="width: 100px" src="https://www.sendx.io/hubfs/SendPost_August2021/images/SendX-By-Logo.svg" width="100" /> -->
<br>API
</h1>
</div>

The following utility functions are designed to interact with the PokeAPI to retrieve information about Pokemon. These functions are asynchronous and utilize the Fetch API for making HTTP requests.


# Functions

## `getPokemonList`

This function fetches the information of the first 151 Pokemon.

### Usage

```jsx
import { getPokemonList } from "./path-to-api-utils";

// Example usage:
const pokemonList = await getPokemonList();
```
#### `Returns` An array of objects, each representing a Pokemon with `name` and `url` properties.

## `getPokemon(name: string)`

This function retrieves detailed information about a specific Pokemon based on its name.

### Usage

```jsx
import { getPokemon } from "./path-to-api-utils";

// Example usage:
const pikachuData = await getPokemon("pikachu");
```
#### `Returns` An object containing detailed information about the specified Pokemon.

