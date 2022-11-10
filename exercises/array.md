
1. Log all numbers from 0 to 15.
<details>
<summary>Solution</summary>

```js
Array(16).fill().forEach((value, index) => {
    console.log(index)
})
```
</details>

2. Log all numbers from 12 to 24.
<details>
<summary>Solution</summary>

```js
Array(25).fill().forEach((value, index) => {
    if (12 <= index && index <= 24) {
        console.log(index)
    }
})
```
</details>

3. Log all numbers from 1 to 10 except 4 and 7.
<details>
<summary>Solution</summary>

```js
Array(11).fill().forEach((value, index) => {
    if (
        1 <= index && index <= 10 && // interval 1-10
        index !== 4 && // except 4
        index !== 7 // except 7
    ) {
        console.log(index)
    }
})
```
</details>

4. Create an array with the first five numbers from 1 to 5.
<details>
<summary>Solution</summary>

```js
const array = Array(5).fill().map((value, index) => {
    return index + 1
})
```
</details>

5. Create a function that receives an argument "length" and returns an array with the first numbers from 1 to "length".
<details>
<summary>Solution</summary>

```js
const generateArrayOfLength = (length) => {
    return Array(length).fill().map((value, index) => {
        return index + 1
    })
}
```
</details>

6. Create a function that logs all numbers from 1 to 10 except the numbers of given array that should be excluded. Example:

```js
printNumbersExcept([3, 6, 7])

// 1
// 2
// 4
// 5
// 8
// 9
// 10
```
<details>
<summary>Solution</summary>

```js
const printNumbersExcept = (excludedArray) => {
    Array(11).fill().map((value, index) => {
        if (
            1 <= index && index <= 10 && // interval 1-10
            !excludedArray.includes(index) // index is not included in excludedArray
        ) {
            console.log(index)
        }
    })
}
```
</details>

7. Create a function to reverse the order of the characters in a string

<details>
<summary>Solution</summary>

```js
const reverseString = (string) => {
    return string.split('').reverse().join('')
}
```
</details>

8. Create a function that receives an array of numbers and returns the maximum value.

<details>
<summary>Solution</summary>

```js
const findMaxValue = (array) => {
    let maxValue = 0
    array.forEach((value) => {
        if (value > maxValue) {
            maxValue = value
        }
    })
    return maxValue
}
```
</details>

9. Create a function that returns true if every value of an array is higher or equal to 10.

<details>
<summary>Solution</summary>

```js
const isPerfectScore = (array) => {
    return array.every((value) => value >= 10)
}
```
</details>

10. Create a function that returns true if some value of an array is higher or equal to 40.

<details>
<summary>Solution</summary>

```js
const temperatureHasExcedeed40Degrees = (array) => {
    return array.some((value) => value >= 40)
}
```
</details>

11. Create a function that receives 2 arrays and return the merged array without duplicated values. Example:

```js
unionArrays([3, 6, 7], [2, 3, 4])

// [3,6,7,2,4]
```
<details>
<summary>Solution</summary>

```js
const unionArrays = (array1, array2) => {
    const mergedArray = [...array1, ...array2]
    return mergedArray.filter((value, index) => mergedArray.indexOf(value) === index)
}
```
</details>

12. Create a function that receives 2 arrays and return an array with only the coincident values. Example:
```js
intersectionArrays([3, 6, 7], [2, 3, 4])

// [3]
```
<details>
<summary>Solution</summary>

```js
const intersectionArrays = (array1, array2) => {
    return array1.filter((value) => array2.includes(value))
}
```
</details>

13. Create a function that receives an array of numbers and returns a new array including only the odd numbers.
<details>
<summary>Solution</summary>

```js
const isOdd = (value) => value % 2 === 0
const onlyOddArray = (array) => {
    return array.filter(isOdd)
}
```
</details>

14. Create a function that receives an array of numbers and returns an array of strings indicating if each one is odd or even. Example:
```js
defineOddOrEven([3, 6, 7])

// ['3 is even', '6 is odd', '7 is even']
```
<details>
<summary>Solution</summary>

```js
const isOdd = (value) => value % 2 === 0
const defineOddOrEven = (array) => {
    return array.map((value) => {
        return `${value} is ${isOdd(value) ? 'odd' : 'even'}`
    })
}
```
</details>