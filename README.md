
# Javascript Cheatsheet

## Basics

___

### Boolean type

Declaration
```js
let someBoolean = false
let someBoolean = true
```

___

### Number type

Declaration
```js
let number = 19.91
```
Functions
```js
// Check if variable is not a number
const someBoolean = isNaN('someString') // true
const someBoolean = isNaN(19.91) // false
const someBoolean = isNaN('19.91') // false

// Convert number/string to float number (with decimals)
const someNumber = parseFloat('15.92') // 15.92

// Convert number/string to integer number (without decimals)
const someNumber = parseInt(number) // 19
```
Methods
```js
// Convert number to string 
const someString = number.toString() // '19.91'

// Convert number to string 
const someString = number.toString() // '19.91'

// Define amount of decimals 
const someString = number.toFixed(1) // '19.9'
const someString = number.toFixed(3) // '19.910'
```

___

### String type

Declaration
```js
const string = 'The king is my father'
const string = "The king is my father"

// String templates
const who = 'father'
const string = `The king is my ${who}` // 'The king is my father'
```
Methods
```js
// Check if string starts with substring (case sensitive)
const someBoolean = string.startsWith('The') // true
const someBoolean = string.startsWith('the') // false

// Check if string ends with substring (case sensitive)
const someBoolean = string.endsWith('father') // true

// Replace a substring by other substring
const someString = string.replaceAll('my', 'your') // 'The king is your father'

// Make string lower case
const someString = string.toLowerCase() // 'the king is my father'

// Make string upper case
const someString = string.toUpperCase() // 'THE KING IS MY FATHER'

// Remove start/end spaces
const stringWithSpaces = '  some string with spaces   '
const someString = stringWithSpaces.trim() // 'string with spaces'

// Get length of string
const someNumber = string.length // 21

// Split/get list from string given a substring as separator
const someArray = string.split(' ') // ['The', 'king', 'is', 'my', 'father']
```

___

### Object type

Declaration
```js
const object = {
  name: 'John',
  age: 25,
}
```
Methods
```js
// Get property value 

    // Fixed key
    const someNumber = object.age // 25

     // Variable key
    const key = 'age'
    const someNumber = object[key] // 25


// Add property

    // Fixed key
    object.dni = '123-45-6789'

    // Dynamic key
    const key = 'dni'
    object[key] = '123-45-6789'

    // const object = {
    //   name: 'John',
    //   age: 25,
    //   dni: '123-45-6789',
    // }


// Change property value

    // Fixed key
    object.name = 'John Doe'

     // Variable key
    const key = 'name'
    object[key] = 'John Doe'

    // const object = {
    //   name: 'John Doe',
    //   age: 25,
    // }


// Delete property 

    // Fixed key
    delete object.age

     // Variable key
    const key = 'age'
    delete object[key]

    // const object = {
    //   name: 'John Doe',
    // }
```
Functions
```js
// Get keys as list
const someArray = Object.keys(object) // ['name', 'age']

// Get values as list
const someArray = Object.values(object) // ['John', 25]

// Get keys and values as list
const someArray = Object.entries(object) // [['name', 'John'], ['age', 25]]
```

___

### Array type

Declaration
```js
let array = ['Pais Vasco', 'Islas Cies', 'Cantabria', 'Islas Canarias']
```
Methods
```js
// get length of array
const someNumber = array.length // 4


// Add element to array
array.push('La Alpujarra')
// ['Pais Vasco', 'Islas Cies', 'Cantabria', 'Islas Canarias', 'La Alpujarra']


// Get element of aray given a position
    // Fixed key
    const someString = array[1] // 'Islas Cies'

    // Variable key
    const position = 1
    const someString = array[position] // 'Islas Cies'


// Map to new values given a function
const someArray = array.map((value, position) => {
    return `${value} is at position ${position}`
})
// [
//     'Pais Vasco is at position 0',
//     'Islas Cies is at position 1',
//     'Cantabria is at position 2',
//     'Islas Canarias is at position 3'
// ]


// Filter array given a function. Only 'true' evaluations are added to the result
const someArray = array.filter((value, position) => {
    return value.startsWith('Islas') // boolean
})
// [
//     'Islas Cies',
//     'Islas Canarias'
// ]


// Find first element of an array that satisfies a condition.
const someString = array.find((value, position) => {
    return value.startsWith('Islas')
})
// 'Islas Cies',


// Check if SOME value of the array satisfies a condition.
const someBoolean = array.some((value, position) => {
    return value.startsWith('Islas')
})
// true


// Check if EVERY of the array value satisfies a condition.
const someBoolean = array.every((value, position) => {
    return value.startsWith('Islas')
})
// false


// Check if array includes a value
const someBoolean = array.includes('Cantabria') // true


// Join array of strings in single string (giving a separator)
const someString = array.join('-') // 'País Vasco-Islas Cies-Cantabria-Islas Canarias'


// Reverse order of array
const someArray = array.reverse() // ['Islas Canarias', 'Cantabria', 'Islas Cies', 'País Vasco']
```

Order functions
```js
// Order from min to max
const points = [40, 100, 1, 5, 25, 10]
points.sort((a, b) => a - b) // [1, 5, 10, 25, 40, 100]

// Order from max to min
const points = [40, 100, 1, 5, 25, 10]
points.sort((a, b) => b - a) // [100, 40, 25, 10, 5, 1]

// Order alphabetically
let array = ['Pais Vasco', 'Islas Cies', 'Cantabria', 'Islas Canarias']
array.sort((a, b) => a.localeCompare(b)) // ['Cantabria', 'Islas Canarias', 'Islas Cies', 'Pais Vasco']
```
