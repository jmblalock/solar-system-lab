![GA-logo](https://camo.githubusercontent.com/6ce15b81c1f06d716d753a61f5db22375fa684da/68747470733a2f2f67612d646173682e73332e616d617a6f6e6177732e636f6d2f70726f64756374696f6e2f6173736574732f6c6f676f2d39663838616536633963333837313639306533333238306663663535376633332e706e67)

# Solar System Lab

| Title: | Solar system lab | 
|:---:|:---:|
| Class: | sei | 
| Creator: | GA Instructional Team |
| Topics: | Objects <br> Mixed Datatypes <br> Complex Data Structures<br> `this` |



## Setup

Do the usual thing and put your answers in `app.js`


## Nested data: Arrays of Objects


### The solar system, part 1

The following data structure, `solarSystem`, is a common data structure: an **array** of **objects**. You will see this particular data structure more and more as you venture into JSON and servers. This one is an **array** of **objects** which also contains **arrays**.

Note that the objects do not have names. They are just anynmous objects listed in an array. 

Given the following data structure of arrays and objects:

```javascript
const solarSystem = [
	{ name: "Mercury", ringSystem: false, moons: [] },
	{ name: "Venus", ringSystem: false, moons: [] },
	{ name: "Earth", ringSystem: false, moons: ["The Moon"] },
	{ name: "Mars", ringSystem: false, moons: ["Phobos", "Deimos"] },
	{ name: "Jupiter", ringSystem: true, moons: ["Europa", "Ganymede", "Io", "Callisto"] },
	{ name: "Saturn", ringSystem: true, moons: ["Titan", "Enceladus", "Rhea", "Mimas"] },
	{ name: "Uranus", ringSystem: true, moons: ["Miranda", "Titania", "Ariel", "Umbriel"] },
	{ name: "Neptune", ringSystem: true, moons: ["Triton", "Nereid"] }
];

```

Write Javascript that does the following:

EXAMPLE:
- Print the boolean for Mercury's ringSystem

ANSWER

```javascript
console.log(solarSystem[0].ringSystem)
```


1. Print the array of Jupiter's moons to the console (no _for loop_, just print the entire array).
2. Print the name of Neptune's moon "Nereid" to the console.
3. Add a new moon called "Endor" to Venus' moons array.
4. Add a Pluto object to the solarSystem array using .push. The object should contain Pluto's name, ringSystem boolean, and moons array (which includes "Charon").
5. Add a new key value pair to the the Earth object: the key should be 'diameter', and the value should be Earth's diameter in miles represented as a string.
6. Change Mercury's ringSystem boolean to true.
7. Change Uranus' moon "Umbriel" to "Oberon"
8. Iterate through the solarSystem array and print only the objects that have a ringSystem (where ringSystem: true), and ignore the others. You want to make a loop that goes over each item in the array, and include an if statement.

Expected result for question 8

> `{ name: 'Mercury', ringSystem: true, moons: [] }`
> 
> `{ name: 'Jupiter', ringSystem: true, moons: [ 'Europa', 'Ganymede', 'Io', 'Callisto' ] }`
> 
> `{ name: 'Saturn', ringSystem: true, moons: [ 'Titan', 'Enceladus', 'Rhea', 'Mimas' ] }`
> 
> `{ name: 'Uranus', ringSystem: true, moons: [ 'Miranda', 'Titania', 'Ariel', 'Oberon' ] }`
> 
> `{ name: 'Neptune', ringSystem: true, moons: [ 'Triton', 'Nereid' ] }`

<br>
<hr>

## The solar system, part 2

Copy this **object** into your file (it's big). Remember, this is an **object of objects** not an array of objects.

```javascript
const system = { 
    Mercury: { 
        radiusp: 'same',
        name: 'Mercury',
        density: 5.43,
        tilt: 2,
        image: 'textures/mercury.gif',
        rotationperiod: 1408,
        period: 0.24,
        radiuse: 2439,
        satellites: 0,
        au: 0.3871,
        eccentricity: 0.206,
        velocity: 47.89,
        mass: 0.06,
        inclination: 7 
    },
    Venus: { 
        radiusp: 'same',
        name: 'Venus',
        density: 5.25,
        tilt: 177.3,
        image: 'textures/venus.gif',
        rotationperiod: 5832,
        period: 0.62,
        radiuse: 6052,
        satellites: 0,
        au: 0.7233,
        eccentricity: 0.007,
        velocity: 35.04,
        mass: 0.82,
        inclination: 3.4 
    },
    Earth: { 
        radiusp: 6357,
        name: 'Earth',
        density: 5.52,
        tilt: 23.45,
        image: 'textures/earth.gif',
        rotationperiod: 23.93,
        period: 1,
        radiuse: 6378,
        satellites: 1,
        au: 1,
        eccentricity: 0.017,
        velocity: 29.79,
        mass: 1,
        inclination: 0 
    },
    Mars: {
        radiusp: 3380,
        name: 'Mars',
        density: 3.95,
        tilt: 25.19,
        image: 'textures/mars.gif',
        rotationperiod: 24.62,
        period: 1.88,
        radiuse: 3397,
        satellites: 2,
        au: 1.524,
        eccentricity: 0.093,
        velocity: 24.14,
        mass: 0.11,
        inclination: 1.85 
    },
    Jupiter: { 
        radiusp: 66854,
        name: 'Jupiter',
        density: 1.33,
        tilt: 3.12,
        image: 'textures/jupiter.gif',
        rotationperiod: 9.92,
        period: 11.86,
        radiuse: 71490,
        satellites: '69',
        au: 5.203,
        eccentricity: 0.048,
        velocity: 13.06,
        mass: 317.89,
        inclination: 1.3 
    }, 
    Saturn: { 
        radiusp: 54360,
        name: 'Saturn',
        density: 0.69,
        tilt: 26.73,
        image: 'textures/saturn.gif',
        rotationperiod: 10.66,
        period: 29.46,
        radiuse: 60268,
        satellites: 30,
        au: 9.539,
        eccentricity: 0.056,
        velocity: 9.64,
        mass: 95.18,
        inclination: 2.49 
    },
    Uranus: { 
        radiusp: 24973,
        name: 'Uranus',
        density: 1.29,
        tilt: 97.86,
        image: 'textures/uranus.gif',
        rotationperiod: 17.24,
        period: 84.01,
        radiuse: 25559,
        satellites: 24,
        au: 19.19,
        eccentricity: 0.046,
        velocity: 6.81,
        mass: 14.53,
        inclination: 0.77 
    },
    Neptune: { 
        radiusp: 24340,
        name: 'Neptune',
        density: 1.64,
        tilt: 29.6,
        image: 'textures/neptune.gif',
        rotationperiod: 16.11,
        period: 164.79,
        radiuse: 25269,
        satellites: 8,
        au: 30.06,
        eccentricity: 0.01,
        velocity: 5.43,
        mass: 17.14,
        inclination: 1.77 
    },
    Pluto: { 
        radiusp: 'same',
        name: 'Pluto',
        density: 2.03,
        tilt: 122.46,
        image: 'textures/pluto.gif',
        rotationperiod: 153.3,
        period: 248.54,
        radiuse: 1160,
        satellites: 1,
        au: 39.48,
        eccentricity: 0.248,
        velocity: 4.74,
        mass: 0.002,
        inclination: 17.15 
    } 
}
```

Write the commands you would use to do the following:

1. console.log the mass of Mercury
2. console.log the eccentricity of Venus
3. console.log the sum of the number of satellites of Jupiter, Saturn, Uranus, and Neptune (131)
4. Write a conditional that checks if Mercury's `radiusp` is a string (remember the `typeof` command). If Mercury's `radiusp` is a string, change the value to be the same as its `radiuse` value. (`radiusp` is radius at the poles, `radiuse` is radius at the equator).
5. console.log Mercury's `radiusp` (should be 2439, not 'same').
6. Find the difference between Jupiter's **momentum** and Pluto's **momentum**. (To get momentum, you'll want the product of **velocity** and **mass**). 


### Planet X
Outside of any of these predefined solar system objects, make your own object called **PlanetX**. Give PlanetX the same properties as a planet within `system` (eg. density, tilt, mass) and give it made-up values.

Without directly altering either the `system` object or the `PlanetX` object, include planetX as a property of system. (Your planetX object is a planet within the system).

When you `console.log(system)`, planetX should be appear as a planet in the system.

---

# Hungry for more?

## A. Weather Lab

Complete this [advanced object lab, which uses weather forecast data](https://git.generalassemb.ly/sf-sei-3/weather-object-lab).

---

## B. Sorting an array of objects

Complete this [activity about the Array method `.sort()`](https://git.generalassemb.ly/WebDev-Connected-Classroom/sort-activity) which is very powerful and can be used to sort arrays in a number of ways.  
