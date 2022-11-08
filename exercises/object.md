1. Set `age` to `31` in the following object:
```js
const person = {
    name: 'James',
    age: 20,
}
```
<details>
<summary>Solution</summary>

```js
person.age = 31
```
</details>


2. Set a new key called `fav-music` with value `techno` in the following object:
```js
const person = {
    name: 'James',
    age: 20,
}
```
<details>
<summary>Solution</summary>

```js
person['fav-music'] = 'techno'
```
</details>

3. Delete the `name` and `fav-music` key from an object in a variable named `person`.

<details>
<summary>Solution</summary>

```js
delete person['name']
delete person['fav-music']
```
</details>


4. Create a function that prints all the keys of an object. Example:
```js
printKeys({a: 1, b: 2})
// a
// b
```

<details>
<summary>Solution</summary>

```js
const printKeys = (object) => {
    Object.keys(object).forEach((value) => {
        console.log(value)
    })
}
```
</details>

5. Create a function that prints all the values of an object. Example:
```js
printValues({a: 1, b: 2})
// 1
// 2
```

<details>
<summary>Solution</summary>

```js
const printValues = (object) => {
    Object.values(object).forEach((value) => {
        console.log(value)
    })
}
```
</details>

6. Create a function that return `true` if some value of an object is `'techno'`:

<details>
<summary>Solution</summary>

```js
const someValueIsTechno = (object) => {
    return Object.values(object).includes('techno')
}
```
</details>

7. Create a function to convert an array of strings to keys of an object of value `0`. Example:
```js
convertToObject(['a', 'b'])

// {a: 0, b: 0}
```

<details>
<summary>Solution</summary>

```js
const convertToObject = (array) => {
    let emptyObject = {}
    array.forEach((value) => {
        emptyObject[value] = 0
    })
    return emptyObject
}
```
</details>

8. Create a function that receives an object and an array. It should remove all the keys that are found in the array. Example:

```js
removeFromObject({a: 1, b: 2}, ['b'])

// {a: 1}
```

<details>
<summary>Solution</summary>

```js
const removeFromObject = (object, array) => {
    array.forEach((value) => {
        delete object[value]
    })
    return object
}
```
</details>

9. Create a function to merge 2 objects. Keys of first object will have preference over second one.

```js
mergeObjects({a: 1, b: 2}, {a: 1, c: 3})

// {a: 1, b: 2, c: 3}
```
<details>
<summary>Solution</summary>

```js
// Manual solution
const mergeObjects = (object1, object2) => {
    Object.keys(object2).forEach((key) => {
        if (!object1[key]) {
            object1[key] = object2[key]
        }
    })
    return object
}
// Built-in solutions
const mergeObjects = (object1, object2) => {
    return Object.assign(object1, object2)
}
const mergeObjects = (object1, object2) => {
    return {...object1, ...object2}
}
```
</details>