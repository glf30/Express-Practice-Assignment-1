# Express-Practice-Assignment-1

## Goals
- Create a server using the Express module  
- Create an API that serves data based on the URL request  
- Practice sending JSON responses  

---

## Food Truck Locator API 

You are now an intern for the **NYC Food Truck Association**! Tourists and office workers constantly ask where food trucks are located and what kind of food they serve. The association wants a simple API that responds with food truck data based on the URL.

For this assignment, you will work with the following data:

```js
const foodTrucks = {
  downtown: [
    {
      name: "Big Apple Burgers",
      cuisine: ["burgers", "fries"],
      open: true
    },
    {
      name: "Taco Loco",
      cuisine: ["mexican", "tacos"],
      open: false
    },
    {
      name: "Curry in a Hurry",
      cuisine: ["indian"],
      open: true
    },
    {
      name: "Impastable",
      cuisine: ["italian", "pasta"],
      open: true
    },
    {
      name: "Bao Down",
      cuisine: ["chinese", "dumplings"],
      open: true
    },
    {
      name: "Green Garden",
      cuisine: ["vegetarian", "vegan"],
      open: false
    },
    {
      name: "Pizza My Heart",
      cuisine: ["italian", "pizza"],
      open: true
    },
    {
      name: "Taqueria Express",
      cuisine: ["mexican", "tacos", "burritos"],
      open: true
    },
    {
      name: "Falafel Fusion",
      cuisine: ["middle eastern", "vegetarian", "falafel"],
      open: true
    },
    {
      name: "The Noodle Cart",
      cuisine: ["chinese", "noodles"],
      open: false
    },
    {
      name: "Veggie Delight",
      cuisine: ["vegetarian", "vegan", "salads"],
      open: true
    },
    {
      name: "Pasta Bella",
      cuisine: ["italian", "pasta"],
      open: false
    },
    {
      name: "Smoky Joe's BBQ",
      cuisine: ["bbq", "burgers"],
      open: true
    },
    {
      name: "Slice of Heaven",
      cuisine: ["pizza", "italian"],
      open: false
    },
    {
      name: "Sushi Street",
      cuisine: ["japanese", "sushi"],
      open: true
    }
  ],

  midtown: [
    {
      name: "Slice City",
      cuisine: ["pizza"],
      open: true
    },
    {
      name: "Wok This Way",
      cuisine: ["chinese", "noodles"],
      open: true
    },
    {
      name: "Falafel King",
      cuisine: ["middle eastern", "vegetarian"],
      open: false
    },
    {
      name: "El Toro Rojo",
      cuisine: ["mexican", "tacos"],
      open: true
    },
    {
      name: "Pasta Express",
      cuisine: ["italian", "pasta"],
      open: false
    },
    {
      name: "Cheese Please",
      cuisine: ["burgers", "cheese"],
      open: true
    },
    {
      name: "Veggie Vibes",
      cuisine: ["vegetarian", "vegan"],
      open: true
    },
    {
      name: "Napoli on Wheels",
      cuisine: ["italian", "pizza"],
      open: true
    },
    {
      name: "Taco Town",
      cuisine: ["mexican", "tacos", "burritos"],
      open: false
    },
    {
      name: "Golden Dumplings",
      cuisine: ["chinese", "dumplings"],
      open: true
    },
    {
      name: "Bombay Bites",
      cuisine: ["indian", "curry"],
      open: true
    },
    {
      name: "The Green Fork",
      cuisine: ["vegetarian", "salads"],
      open: false
    },
    {
      name: "BBQ Boulevard",
      cuisine: ["bbq", "burgers"],
      open: true
    },
    {
      name: "Pasta Parade",
      cuisine: ["italian", "pasta"],
      open: true
    },
    {
      name: "Tokyo Treats",
      cuisine: ["japanese", "sushi"],
      open: false
    }
  ],

  uptown: [
    {
      name: "Northern BBQ",
      cuisine: ["bbq", "burgers"],
      open: true
    },
    {
      name: "Rolling Sushi",
      cuisine: ["japanese", "sushi"],
      open: true
    },
    {
      name: "Veggie Wheels",
      cuisine: ["vegetarian", "vegan"],
      open: true
    },
    {
      name: "Pasta World",
      cuisine: ["italian", "pasta"],
      open: true
    },
    {
      name: "Pizza Planet",
      cuisine: ["pizza", "italian"],
      open: false
    },
    {
      name: "Taco Fiesta",
      cuisine: ["mexican", "tacos"],
      open: true
    },
    {
      name: "Spice Route",
      cuisine: ["indian", "curry"],
      open: false
    },
    {
      name: "The Burger Bus",
      cuisine: ["burgers", "fries"],
      open: true
    },
    {
      name: "Vegan Voyage",
      cuisine: ["vegetarian", "vegan"],
      open: false
    },
    {
      name: "Little Italy Truck",
      cuisine: ["italian", "pasta"],
      open: true
    },
    {
      name: "Chinatown Express",
      cuisine: ["chinese", "dumplings", "noodles"],
      open: true
    },
    {
      name: "Taco Supreme",
      cuisine: ["mexican", "tacos", "burritos"],
      open: false
    },
    {
      name: "Garden on Wheels",
      cuisine: ["vegetarian", "salads", "vegan"],
      open: true
    },
    {
      name: "Pizza Pocket",
      cuisine: ["pizza"],
      open: true
    },
    {
      name: "Mediterranean Magic",
      cuisine: ["middle eastern", "vegetarian", "falafel"],
      open: true
    }
  ]
};

```

## API Requirements
- If the URL ends in /, send back the entire foodTrucks object
- If the URL ends in /downtown, send back only the downtown food trucks
- If the URL ends in /midtown, send back only the midtown food trucks
- If the URL ends in /uptown, send back only the uptown food trucks
- If the URL ends in /open, return only food trucks where open is true
- If the URL ends in /vegetarian, return only trucks that serve "vegetarian"
- If the URL ends in /italianOpen, return only trucks that serve "italian" and are open
- If the URL ends in /openPizzaOrTacos, return only open food trucks that serve either "pizza" or "tacos".
- If the URL ends in /multipleCuisines, return only food trucks that serve more than one cuisine.
- If the URL ends in /openCounts, return an object containing the number of open food trucks in each neighborhood.
- If the URL ends in /mostCuisines, return the food truck(s) that serves the greatest number of cuisines.
- If the URL ends in anything else, respond with a failure message.
