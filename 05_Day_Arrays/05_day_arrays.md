<div align="center">
  <h1> 30 Days Of JavaScript: Arrays</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/asabeneh?style=social">
  </a>

  <sub>Author:
  <a href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br>
  <small> January, 2020</small>
  </sub>
</div>

[<< Day 4](../04_Day_Conditionals/04_day_conditionals.md) | [Day 6 >>](../06_Day_Loops/06_day_loops.md)

![Day 5](../images/banners/day_1_5.png)

- [📔 Day 5](#-day-5)
	- [Arrays](#arrays)
		- [How to create an empty array](#how-to-create-an-empty-array)
		- [How to create an array with values](#how-to-create-an-array-with-values)
		- [Creating an array using split](#creating-an-array-using-split)
		- [Accessing array items using index](#accessing-array-items-using-index)
		- [Modifying array element](#modifying-array-element)
		- [Methods to manipulate array](#methods-to-manipulate-array)
			- [Array Constructor](#array-constructor)
			- [Creating static values with fill](#creating-static-values-with-fill)
			- [Concatenating array using concat](#concatenating-array-using-concat)
			- [Getting array length](#getting-array-length)
			- [Getting index an element in arr array](#getting-index-an-element-in-arr-array)
			- [Getting last index of an element in array](#getting-last-index-of-an-element-in-array)
			- [Checking array](#checking-array)
			- [Converting array to string](#converting-array-to-string)
			- [Joining array elements](#joining-array-elements)
			- [Slice array elements](#slice-array-elements)
			- [Splice method in array](#splice-method-in-array)
			- [Adding item to an array using push](#adding-item-to-an-array-using-push)
			- [Removing the end element using pop](#removing-the-end-element-using-pop)
			- [Removing an element from the beginning](#removing-an-element-from-the-beginning)
			- [Add an element from the beginning](#add-an-element-from-the-beginning)
			- [Reversing array order](#reversing-array-order)
			- [Sorting elements in array](#sorting-elements-in-array)
		- [Array of arrays](#array-of-arrays)
	- [💻 Exercise](#-exercise)
		- [Exercise: Level 1](#exercise-level-1)
		- [Exercise: Level 2](#exercise-level-2)
		- [Exercise: Level 3](#exercise-level-3)

# 📔 Day 5

## מערכים

בניגוד למשתנים, מערך יכול לאחסן _ערכים רבים_. לכל ערך במערך יש _אינדקס_, ולכל אינדקס יש _הפניה בכתובת זיכרון_. ניתן לגשת לכל ערך באמצעות ה-_אינדקס_ שלהם. האינדקס של מערך מתחיל מ-_0_, והאינדקס של האלמנט האחרון קטן באחד מאורך המערך.

מערך הוא אוסף של סוגי נתונים שונים אשר מסודרים וניתנים לשינוי. מערך מאפשר אחסון אלמנטים כפולים וסוגי נתונים שונים. מערך יכול להיות ריק, או שיש לו ערכי סוגי נתונים שונים.

### כיצד ליצור מערך ריק

ב-JavaScript, אנו יכולים ליצור מערך בדרכים שונות. הבה נראה דרכים שונות ליצור מערך.
נפוץ מאוד להשתמש ב-_const_ במקום ב-_let_ כדי להכריז על משתנה מערך. אם אתה משתמש ב-const זה אומר שאתה לא משתמש בשם המשתנה הזה שוב להקצות לו ערך אחר במקום המערך הנוכחי.

- שימוש בבנאי מערך

```js
// syntax
const arr = Array()
// או
// let arr = new Array()
console.log(arr) // []
```

- שימוש בסוגריים מרובעים ([])

```js
// syntax
// זו הדרך המומלצת ביותר ליצור רשימה ריקה
const arr = []
console.log(arr)
```

### כיצד ליצור מערך עם ערכים

מערך עם ערכים ראשוניים. אנו משתמשים במאפיין _length_ כדי למצוא את האורך של מערך.

```js
const numbers = [0, 3.14, 9.81, 37, 98.6, 100] // מערך מספרים
const fruits = ['banana', 'orange', 'mango', 'lemon'] // מערך של מחרוזות, פירות
const vegetables = ['Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot'] // מערך של מחרוזות, ירקות
const animalProducts = ['milk', 'meat', 'butter', 'yoghurt'] // מערך של מחרוזות, מוצרים
const webTechs = ['HTML', 'CSS', 'JS', 'React', 'Redux', 'Node', 'MongDB'] // מגוון טכנולוגיות אינטרנט
const countries = ['Finland', 'Denmark', 'Sweden', 'Norway', 'Iceland'] // מערך של מחרוזות, מדינות

// הדפס את המערך ואורכו

console.log('Numbers:', numbers)
console.log('Number of numbers:', numbers.length)

console.log('Fruits:', fruits)
console.log('Number of fruits:', fruits.length)

console.log('Vegetables:', vegetables)
console.log('Number of vegetables:', vegetables.length)

console.log('Animal products:', animalProducts)
console.log('Number of animal products:', animalProducts.length)

console.log('Web technologies:', webTechs)
console.log('Number of web technologies:', webTechs.length)

console.log('Countries:', countries)
console.log('Number of countries:', countries.length)
```

```sh
Numbers: [0, 3.14, 9.81, 37, 98.6, 100]
Number of numbers: 6
Fruits: ['banana', 'orange', 'mango', 'lemon']
Number of fruits: 4
Vegetables: ['Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot']
Number of vegetables: 5
Animal products: ['milk', 'meat', 'butter', 'yoghurt']
Number of animal products: 4
Web technologies: ['HTML', 'CSS', 'JS', 'React', 'Redux', 'Node', 'MongDB']
Number of web technologies: 7
Countries: ['Finland', 'Estonia', 'Denmark', 'Sweden', 'Norway']
Number of countries: 5
```

- למערך יכולים להיות פריטים מסוגי נתונים שונים

```js
const arr = [
    'Asabeneh',
    250,
    true,
    { country: 'Finland', city: 'Helsinki' },
    { skills: ['HTML', 'CSS', 'JS', 'React', 'Python'] }
] // arr containing different data types
console.log(arr)
```

### יצירת מערך באמצעות פיצול

כפי שראינו ביום הקודם, אנו יכולים לפצל מחרוזת במיקומים שונים, ונוכל לשנות למערך. הבה נראה את הדוגמאות שלהלן.

```js
let js = 'JavaScript'
const charsInJavaScript = js.split('')

console.log(charsInJavaScript) // ["J", "a", "v", "a", "S", "c", "r", "i", "p", "t"]

let companiesString = 'Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon'
const companies = companiesString.split(',')

console.log(companies) // ["Facebook", " Google", " Microsoft", " Apple", " IBM", " Oracle", " Amazon"]
let txt =
  'I love teaching and empowering people. I teach HTML, CSS, JS, React, Python.'
const words = txt.split(' ')

console.log(words)
// the text has special characters think how you can just get only the words
// ["I", "love", "teaching", "and", "empowering", "people.", "I", "teach", "HTML,", "CSS,", "JS,", "React,", "Python"]
```

### גישה לפריטי מערך באמצעות אינדקס

אנו ניגשים לכל אלמנט במערך באמצעות האינדקס שלו. אינדקס מערך מתחיל מ-0. התמונה למטה מציגה בבירור את האינדקס של כל אלמנט במערך.

![arr index](../images/array_index.png)

```js
const fruits = ['banana', 'orange', 'mango', 'lemon']
let firstFruit = fruits[0] // אנו ניגשים לפריט הראשון באמצעות האינדקס שלו

console.log(firstFruit) // banana

secondFruit = fruits[1]
console.log(secondFruit) // orange

let lastFruit = fruits[3]
console.log(lastFruit) // lemon
// Last index can be calculated as follows

let lastIndex = fruits.length - 1
lastFruit = fruits[lastIndex]

console.log(lastFruit)  // lemon
```

```js
const numbers = [0, 3.14, 9.81, 37, 98.6, 100]  // קבוצה של מספרים

console.log(numbers.length)  // => לדעת את גודל המערך, שהוא 6
console.log(numbers)         // -> [0, 3.14, 9.81, 37, 98.6, 100]
console.log(numbers[0])      //  -> 0
console.log(numbers[5])      //  -> 100

let lastIndex = numbers.length - 1;
console.log(numbers[lastIndex]) // -> 100
```

```js
const webTechs = [
  'HTML',
  'CSS',
  'JavaScript',
  'React',
  'Redux',
  'Node',
  'MongoDB'
] // רשימה של טכנולוגיות אינטרנט

console.log(webTechs)        // כל פריטי המערך
console.log(webTechs.length) // => לדעת את גודל המערך, שהוא 7
console.log(webTechs[0])     //  -> HTML
console.log(webTechs[6])     //  -> MongoDB

let lastIndex = webTechs.length - 1
console.log(webTechs[lastIndex]) // -> MongoDB
```

```js
const countries = [
  'Albania',
  'Bolivia',
  'Canada',
  'Denmark',
  'Ethiopia',
  'Finland',
  'Germany',
  'Hungary',
  'Ireland',
  'Japan',
  'Kenya'
] // רשימת מדינות

console.log(countries)      // -> כל המדינות במערך
console.log(countries[0])   //  -> Albania
console.log(countries[10])  //  -> Kenya

let lastIndex = countries.length - 1;
console.log(countries[lastIndex]) //  -> Kenya
```

```js
const shoppingCart = [
  'Milk',
  'Mango',
  'Tomato',
  'Potato',
  'Avocado',
  'Meat',
  'Eggs',
  'Sugar'
] // רשימת מוצרי מזון

console.log(shoppingCart) // -> כל עגלת הקניות במערך
console.log(shoppingCart[0]) //  -> Milk
console.log(shoppingCart[7]) //  -> Sugar

let lastIndex = shoppingCart.length - 1;
console.log(shoppingCart[lastIndex]) //  -> Sugar
```

### Modifying array element

מערך ניתן לשינוי. לאחר יצירת מערך, נוכל לשנות את התוכן של רכיבי המערך.

```js
const numbers = [1, 2, 3, 4, 5]
numbers[0] = 10      // שינוי 1 (אינדקס 0) ל-10
numbers[1] = 20      // שינוי 2 (אינדקס 1) ל-20

console.log(numbers) // [10, 20, 3, 4, 5]

const countries = [
  'Albania',
  'Bolivia',
  'Canada',
  'Denmark',
  'Ethiopia',
  'Finland',
  'Germany',
  'Hungary',
  'Ireland',
  'Japan',
  'Kenya'
]

countries[0] = 'Afghanistan'  // מחליפה את אלבניה באפגניסטן
let lastIndex = countries.length - 1
countries[lastIndex] = 'Korea' // מחליף את קניה בקוריאה

console.log(countries)
```

```sh
["Afghanistan", "Bolivia", "Canada", "Denmark", "Ethiopia", "Finland", "Germany", "Hungary", "Ireland", "Japan", "Korea"]
```

### מתודות שונות למערך

ישנן מתודות שונות לתפעל מערך. אלו הן כמה מהמתודות הזמינות להתמודדות עם מערכים:_Array, length, concat, indexOf, slice, splice, join, toString, include, lastIndexOf, isArray, fill, push, pop, shift, unshift_

#### בנאי מערך

מערך: כדי ליצור מערך.

```js
const arr = Array() // יוצר מערך ריק
console.log(arr)

const eightEmptyValues = Array(8) // זה יוצר שמונה ערכים ריקים
console.log(eightEmptyValues) // [empty x 8]
```

#### יצירת ערכים סטטיים עם מילוי

fill: מלא את כל רכיבי המערך בערך סטטי

```js
const arr = Array() // יוצר מערך ריק
console.log(arr)

const eightXvalues = Array(8).fill('X') // 'X'-זה יוצר שמונה ערכי אלמנט מלאים ב 
console.log(eightXvalues) // ['X', 'X','X','X','X','X','X','X']

const eight0values = Array(8).fill(0) // 'זה יוצר שמונה ערכי אלמנט מלאים ב-'0
console.log(eight0values) // [0, 0, 0, 0, 0, 0, 0, 0]

const four4values = Array(4).fill(4) // 'זה יוצר 4 ערכי אלמנט מלאים ב-'4
console.log(four4values) // [4, 4, 4, 4]
```

#### שרשור מערך באמצעות concat

concat: כדי לשרשר שני מערכים.

```js
const firstList = [1, 2, 3]
const secondList = [4, 5, 6]
const thirdList = firstList.concat(secondList)

console.log(thirdList) // [1, 2, 3, 4, 5, 6]
```

```js
const fruits = ['banana', 'orange', 'mango', 'lemon']                 // מערך פירות
const vegetables = ['Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot'] // מערך ירקות
const fruitsAndVegetables = fruits.concat(vegetables)                 // לשרשר את שני המערכים

console.log(fruitsAndVegetables)
```

```sh
["banana", "orange", "mango", "lemon", "Tomato", "Potato", "Cabbage", "Onion", "Carrot"]
```

#### קבלת אורך מערך

length: לדעת את גודל המערך

```js
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.length) // -> 5 הוא גודל המערך
```

#### קבלת אינדקס אלמנט במערך arr

indexOf: כדי לבדוק אם פריט קיים במערך. אם הוא קיים הוא מחזיר את האינדקס אחרת הוא מחזיר -1.

```js
const numbers = [1, 2, 3, 4, 5]

console.log(numbers.indexOf(5)) // -> 4
console.log(numbers.indexOf(0)) // -> -1
console.log(numbers.indexOf(1)) // -> 0
console.log(numbers.indexOf(6)) // -> -1
```

בדוק אלמנט אם הוא קיים במערך.
- בדוק פריטים ברשימה
  
```js
// let us check if a banana exist in the array

const fruits = ['banana', 'orange', 'mango', 'lemon']
let index = fruits.indexOf('banana')  // 0

if(index === -1){
   console.log('This fruit does not exist in the array')  
} else {
    console.log('This fruit does exist in the array')
}
// This fruit does exist in the array

// we can use also ternary here
index === -1 ? console.log('This fruit does not exist in the array'): console.log('This fruit does exist in the array')

// let us check if an avocado exist in the array
let indexOfAvocado = fruits.indexOf('avocado')  // -1, if the element not found index is -1
if(indexOfAvocado === -1){
   console.log('This fruit does not exist in the array')  
} else {
    console.log('This fruit does exist in the array')
}
// This fruit does not exist in the array
```

#### קבלת אינדקס אחרון של אלמנט במערך

lastIndexOf: הוא נותן את המיקום של הפריט האחרון במערך. אם הוא קיים, הוא מחזיר את המדד אחרת הוא מחזיר -1.

```js
const numbers = [1, 2, 3, 4, 5, 3, 1, 2]

console.log(numbers.lastIndexOf(2)) // 7
console.log(numbers.lastIndexOf(0)) // -1
console.log(numbers.lastIndexOf(1)) //  6
console.log(numbers.lastIndexOf(4)) //  3
console.log(numbers.lastIndexOf(6)) // -1
```

includes: כדי לבדוק אם קיים פריט במערך. אם הוא קיים הוא מחזיר את ה-true else הוא מחזיר false.

```js
const numbers = [1, 2, 3, 4, 5]

console.log(numbers.includes(5)) // true
console.log(numbers.includes(0)) // false
console.log(numbers.includes(1)) // true
console.log(numbers.includes(6)) // false

const webTechs = [
  'HTML',
  'CSS',
  'JavaScript',
  'React',
  'Redux',
  'Node',
  'MongoDB'
] // רשימה של טכנולוגיות אינטרנט

console.log(webTechs.includes('Node'))  // true
console.log(webTechs.includes('C'))     // false
```

#### בדיקה אם זה מערך

Array.isArray: כדי לבדוק אם סוג הנתונים הוא מערך

```js
const numbers = [1, 2, 3, 4, 5]
console.log(Array.isArray(numbers)) // true

const number = 100
console.log(Array.isArray(number)) // false
```

#### המרת מערך למחרוזת

toString:ממיר מערך למחרוזת

```js
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.toString()) // 1,2,3,4,5

const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']
console.log(names.toString()) // Asabeneh,Mathias,Elias,Brook
```

#### חיבור אלמנטים של מערך

join: It is used to join the elements of the array, the argument we passed in the join method will be joined in the array and return as a string. By default, it joins with a comma, but we can pass different string parameter which can be joined between the items.

```js
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.join()) // 1,2,3,4,5

const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']

console.log(names.join()) // Asabeneh,Mathias,Elias,Brook
console.log(names.join('')) //AsabenehMathiasEliasBrook
console.log(names.join(' ')) //Asabeneh Mathias Elias Brook
console.log(names.join(', ')) //Asabeneh, Mathias, Elias, Brook
console.log(names.join(' # ')) //Asabeneh # Mathias # Elias # Brook

const webTechs = [
  'HTML',
  'CSS',
  'JavaScript',
  'React',
  'Redux',
  'Node',
  'MongoDB'
] // List of web technologies

console.log(webTechs.join())       // "HTML,CSS,JavaScript,React,Redux,Node,MongoDB"
console.log(webTechs.join(' # '))  // "HTML # CSS # JavaScript # React # Redux # Node # MongoDB"
```

#### Slice array elements

Slice: To cut out a multiple items in range. It takes two parameters:starting and ending position. It doesn't include the ending position.

```js
  const numbers = [1,2,3,4,5]

  console.log(numbers.slice()) // -> it copies all  item
  console.log(numbers.slice(0)) // -> it copies all  item
  console.log(numbers.slice(0, numbers.length)) // it copies all  item
  console.log(numbers.slice(1,4)) // -> [2,3,4] // it doesn't include the ending position
```

#### Splice method in array

Splice: It takes three parameters:Starting position, number of times to be removed and number of items to be added.

```js
  const numbers = [1, 2, 3, 4, 5]
  numbers.splice()
  console.log(numbers)                // -> remove all items

```

```js
  const numbers = [1, 2, 3, 4, 5]
	numbers.splice(0,1)
  console.log(numbers)            // remove the first item
```

```js
  const numbers = [1, 2, 3, 4, 5, 6]
	numbers.splice(3, 3, 7, 8, 9)
  console.log(numbers.splice(3, 3, 7, 8, 9))  // -> [1, 2, 3, 7, 8, 9] //it removes three item and replace three items
```

#### Adding item to an array using push

Push: adding item in the end. To add item to the end of an existing array we use the push method.

```js
// syntax
const arr  = ['item1', 'item2','item3']
arr.push('new item')
console.log(arr)
// ['item1', 'item2','item3','new item']
```

```js
const numbers = [1, 2, 3, 4, 5]
numbers.push(6)
console.log(numbers) // -> [1,2,3,4,5,6]

numbers.pop() // -> remove one item from the end
console.log(numbers) // -> [1,2,3,4,5]
```

```js
let fruits = ['banana', 'orange', 'mango', 'lemon']
fruits.push('apple')
console.log(fruits)    // ['banana', 'orange', 'mango', 'lemon', 'apple']

fruits.push('lime')
console.log(fruits)   // ['banana', 'orange', 'mango', 'lemon', 'apple', 'lime']
```

#### Removing the end element using pop

pop: Removing item in the end.

```js
const numbers = [1, 2, 3, 4, 5]
numbers.pop() // -> remove one item from the end
console.log(numbers) // -> [1,2,3,4]
```

#### Removing an element from the beginning

shift: Removing one array element in the beginning of the array.

```js
const numbers = [1, 2, 3, 4, 5]
numbers.shift() // -> remove one item from the beginning
console.log(numbers) // -> [2,3,4,5]
```

#### Add an element from the beginning

unshift: Adding array element in the beginning of the array.

```js
const numbers = [1, 2, 3, 4, 5]
numbers.unshift(0) // -> add one item from the beginning
console.log(numbers) // -> [0,1,2,3,4,5]
```

#### Reversing array order

reverse: reverse the order of an array.

```js
const numbers = [1, 2, 3, 4, 5]
numbers.reverse() // -> reverse array order
console.log(numbers) // [5, 4, 3, 2, 1]

numbers.reverse()
console.log(numbers) // [1, 2, 3, 4, 5]
```

#### Sorting elements in array

sort: arrange array elements in ascending order. Sort takes a call back function, we will see how we use sort with a call back function in the coming sections.

```js
const webTechs = [
  'HTML',
  'CSS',
  'JavaScript',
  'React',
  'Redux',
  'Node',
  'MongoDB'
]

webTechs.sort()
console.log(webTechs) // ["CSS", "HTML", "JavaScript", "MongoDB", "Node", "React", "Redux"]

webTechs.reverse() // after sorting we can reverse it
console.log(webTechs) // ["Redux", "React", "Node", "MongoDB", "JavaScript", "HTML", "CSS"]
```

### Array of arrays

Array can store different data types including an array itself. Let us create an array of arrays

```js
const firstNums = [1, 2, 3]
const secondNums = [1, 4, 9]

const arrayOfArray =  [[1, 2, 3], [1, 2, 3]]
console.log(arrayOfArray[0]) // [1, 2, 3]

 const frontEnd = ['HTML', 'CSS', 'JS', 'React', 'Redux']
 const backEnd = ['Node','Express', 'MongoDB']
 const fullStack = [frontEnd, backEnd]
 console.log(fullStack)   // [["HTML", "CSS", "JS", "React", "Redux"], ["Node", "Express", "MongoDB"]]
 console.log(fullStack.length)  // 2
 console.log(fullStack[0])  // ["HTML", "CSS", "JS", "React", "Redux"]
 console.log(fullStack[1]) // ["Node", "Express", "MongoDB"]
```

🌕  You are diligent and you have already achieved quite a lot. You have just completed day 5 challenges and you are 5 steps a head in to your way to greatness. Now do some exercises for your brain and for your muscle.

## 💻 Exercise

### Exercise: Level 1

```js
const countries = [
  'Albania',
  'Bolivia',
  'Canada',
  'Denmark',
  'Ethiopia',
  'Finland',
  'Germany',
  'Hungary',
  'Ireland',
  'Japan',
  'Kenya'
]

const webTechs = [
  'HTML',
  'CSS',
  'JavaScript',
  'React',
  'Redux',
  'Node',
  'MongoDB'
]
```

1. Declare an _empty_ array;
2. Declare an array with more than 5 number of elements
3. Find the length of your array
4. Get the first item, the middle item and the last item of the array
5. Declare an array called _mixedDataTypes_, put different data types in the array and find the length of the array. The array size should  be greater than 5
6. Declare an array variable name itCompanies and assign initial values Facebook, Google, Microsoft, Apple, IBM, Oracle and Amazon
7. Print the array using _console.log()_
8. Print the number of companies in the array
9. Print the first company, middle and last company
10. Print out each company
11. Change each company name  to uppercase one by one and print them out
12. Print the array like as a sentence: Facebook, Google, Microsoft, Apple, IBM,Oracle and Amazon are big IT companies.
13. Check if a certain company exists in the itCompanies array. If it exist return the company else return a company is _not found_
14. Filter out companies which have more than one 'o' without the filter method
15. Sort the array using _sort()_ method
16. Reverse the array using _reverse()_ method
17. Slice out the first 3 companies from the array
18. Slice out the last 3 companies from the array
19. Slice out the middle IT company or companies from the array
20. Remove the first IT company from the array
21. Remove the middle IT company or companies from the array
22. Remove the last IT company from the array
23. Remove all IT companies

### Exercise: Level 2

1. Create a separate countries.js file and store the countries array in to this file, create a separate file web_techs.js and store the webTechs array in to this file. Access both file in main.js file
1. First remove all the punctuations and change the string to array and count the number of words in the array

    ```js
    let text =
    'I love teaching and empowering people. I teach HTML, CSS, JS, React, Python.'
    console.log(words)
    console.log(words.length)
    ```

    ```sh
    ["I", "love", "teaching", "and", "empowering", "people", "I", "teach", "HTML", "CSS", "JS", "React", "Python"]
  
    13
    ```

1. In the following shopping cart add, remove, edit items

    ```js
    const shoppingCart = ['Milk', 'Coffee', 'Tea', 'Honey']
    ```

   - add 'Meat' in the beginning of your shopping cart if it has not been already added
   - add Sugar at the end of you shopping cart if it has not been already added
   - remove 'Honey' if you are allergic to honey
   - modify Tea to 'Green Tea'
1. In countries array check if 'Ethiopia' exists in the array if it exists print 'ETHIOPIA'. If it does not exist add to the countries list.
1. In the webTechs array check if Sass exists in the array  and if it exists print 'Sass is a CSS preprocess'. If it does not exist add Sass to the array and print the array.
1. Concatenate the following two variables and store it in a fullStack variable.

    ```js
    const frontEnd = ['HTML', 'CSS', 'JS', 'React', 'Redux']
    const backEnd = ['Node','Express', 'MongoDB']
  
    console.log(fullStack)
    ```

    ```sh
    ["HTML", "CSS", "JS", "React", "Redux", "Node", "Express", "MongoDB"]
    ```

### Exercise: Level 3

1. The following is an array of 10 students ages:

    ```js
    const ages = [19, 22, 19, 24, 20, 25, 26, 24, 25, 24]
    ```

    - Sort the array and find the min and max age
    - Find the median age(one middle item or two middle items divided by two)
    - Find the average age(all items divided by number of items)
    - Find the range of the ages(max minus min)
    - Compare the value of (min - average) and (max - average), use _abs()_ method
1.Slice the first ten countries from the [countries array](https://github.com/Asabeneh/30DaysOfJavaScript/tree/master/data/countries.js)
1. Find the middle country(ies) in the [countries array](https://github.com/Asabeneh/30DaysOfJavaScript/tree/master/data/countries.js)
2. Divide the countries array into two equal arrays if it is even.  If countries array is not even , one more country for the first half.
  
🎉 CONGRATULATIONS ! 🎉

[<< Day 4](../04_Day_Conditionals/04_day_Conditionals.md) | [Day 6 >>](../06_Day_Loops/06_day_loops.md)
