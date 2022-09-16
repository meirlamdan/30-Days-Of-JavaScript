<div align="center">
  <h1> 30 Days Of JavaScript: Booleans, Operators, Date</h1>
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

[<< יום 2](../02_Day_Data_types/02_day_data_types.md) | [Day 4 >>](../04_Day_Conditionals/04_day_conditionals.md)

![Thirty Days Of JavaScript](../images/banners/day_1_3.png)

- [📔 יום 3](#-day-3)
	- [Booleans](#booleans)
		- [Truthy values](#truthy-values)
		- [Falsy values](#falsy-values)
	- [Undefined](#undefined)
	- [Null](#null)
	- [Operators](#operators)
		- [Assignment operators](#assignment-operators)
		- [Arithmetic Operators](#arithmetic-operators)
		- [Comparison Operators](#comparison-operators)
		- [Logical Operators](#logical-operators)
		- [Increment Operator](#increment-operator)
		- [Decrement Operator](#decrement-operator)
		- [Ternary Operators](#ternary-operators)
		- [Operator Precedence](#operator-precedence)
	- [Window Methods](#window-methods)
		- [Window alert() method](#window-alert-method)
		- [Window prompt() method](#window-prompt-method)
		- [Window confirm() method](#window-confirm-method)
	- [Date Object](#date-object)
		- [Creating a time object](#creating-a-time-object)
		- [Getting full year](#getting-full-year)
		- [Getting month](#getting-month)
		- [Getting date](#getting-date)
		- [Getting day](#getting-day)
		- [Getting hours](#getting-hours)
		- [Getting minutes](#getting-minutes)
		- [Getting seconds](#getting-seconds)
		- [Getting time](#getting-time)
	- [💻 Day 3: Exercises](#-day-3-exercises)
		- [Exercises: Level 1](#exercises-level-1)
		- [Exercises: Level 2](#exercises-level-2)
		- [Exercises: Level 3](#exercises-level-3)

#  📔 יום 3

## בוליאנים

סוג נתונים בוליאני מייצג אחד משני הערכים:_true_ או _false_. ערך בוליאני הוא אמת או שקר. השימוש בסוגי נתונים אלה יהיה ברור כאשר אתה מפעיל את אופרטור ההשוואה. כל השוואות מחזירות ערך בוליאני שהוא אמת או שקר.

**דוגמה: ערכים בוליאניים**

```js
let isLightOn = true
let isRaining = false
let isHungry = false
let isMarried = true
let truValue = 4 > 3    // true
let falseValue = 4 < 3  // false
```

הסכמנו שערכים בוליאניים הם נכונים או שקריים.

### ערכי  true

- כל המספרים (חיוביים ושליליים) נכונים מלבד אפס
- כל המחרוזות נכונות מלבד מחרוזת ריקה ('')
- הערך הבולאיני true 

### ערכי false 

- 0
- 0n
- null
- undefined
- NaN
- הערך הבוליאני false 
- '', "", ``, מחרוזת ריקה

טוב לזכור את אותם ערכי אמת וערכים שקר. בסעיף מאוחר יותר, נשתמש בהם עבור תנאים לקבלת החלטות.

## Undefined

אם נכריז על משתנה ואם לא נקצה ערך, הערך לא יהיה מוגדר. בנוסף לכך, אם פונקציה לא מחזירה את הערך, היא לא תהיה מוגדרת.

```js
let firstName
console.log(firstName) //לא מוגדר, מכיוון שהוא עדיין לא מוקצה לערך
```

## Null

```js
let empty = null
console.log(empty) // -> פירושו אין ערך ,null  
```

## Operators

### אופרטור הקצאה

סימן שוויון (=) ב-JavaScript הוא אופרטור הקצאה. הוא משמש כדי להקצות משתנה.

```js
let firstName = 'Asabeneh'
let country = 'Finland'
```

אופרטור הקצאה

![Assignment operators](../images/assignment_operators.png)

### אופרטורים חשבוניים

אופרטורים חשבוניים הם אופרטורים מתמטיים.

- חיבור(+): a + b
- חיסור(-): a - b
- כפל(*): a * b
- חילוק(/): a / b
- מודולס(%): a % b
- אקספוננציאלי (**): a ** b

```js
let numOne = 4
let numTwo = 3
let sum = numOne + numTwo
let diff = numOne - numTwo
let mult = numOne * numTwo
let div = numOne / numTwo
let remainder = numOne % numTwo
let powerOf = numOne ** numTwo

console.log(sum, diff, mult, div, remainder, powerOf) // 7,1,12,1.33,1, 64

```

```js
const PI = 3.14
let radius = 100          // אורך במטר

//הבה נחשב שטח של עיגול
const areaOfCircle = PI * radius * radius
console.log(areaOfCircle)  //  314 m


const gravity = 9.81      // ב-m/s2
let mass = 72             // בקילוגרם

// הבה נחשב משקל של חפץ
const weight = mass * gravity
console.log(weight)        // 706.32 N(Newton)

const boilingPoint = 100  // temperature in oC, boiling point of water
const bodyTemp = 37       // body temperature in oC


// שרשור מחרוזת עם מספרים באמצעות שרבוב מחרוזת
/*
 The boiling point of water is 100 oC.
 Human body temperature is 37 oC.
 The gravity of earth is 9.81 m/s2.
 */
console.log(
  `The boiling point of water is ${boilingPoint} oC.\nHuman body temperature is ${bodyTemp} oC.\nThe gravity of earth is ${gravity} m / s2.`
)
```

### אופרטור השוואה

בתכנות אנו משווים ערכים, אנו משתמשים באופרטורים להשוואה כדי להשוות שני ערכים. אנו בודקים אם ערך גדול או קטן או שווה לערך אחר.

![Comparison Operators](../images/comparison_operators.png)
**דוגמה: אופרטור השוואה**

```js
console.log(3 > 2)              // נכון, כי 3 גדול מ-2
console.log(3 >= 2)             // נכון, כי 3 גדול מ-2
console.log(3 < 2)              // שקר, כי 3 גדול מ-2
console.log(2 < 3)              // נכון, כי 2 זה פחות מ-3
console.log(2 <= 3)             // נכון, כי 2 זה פחות מ-3
console.log(3 == 2)             // שקר, כי 3 אינו שווה ל-2
console.log(3 != 2)             // true, because 3 is not equal to 2
console.log(3 == '3')           // true, compare only value
console.log(3 === '3')          // false, compare both value and data type
console.log(3 !== '3')          // true, compare both value and data type
console.log(3 != 3)             // false, compare only value
console.log(3 !== 3)            // false, compare both value and data type
console.log(0 == false)         // true, equivalent
console.log(0 === false)        // false, not exactly the same
console.log(0 == '')            // true, equivalent
console.log(0 == ' ')           // true, equivalent
console.log(0 === '')           // false, not exactly the same
console.log(1 == true)          // true, equivalent
console.log(1 === true)         // false, not exactly the same
console.log(undefined == null)  // true
console.log(undefined === null) // false
console.log(NaN == NaN)         // false, not equal
console.log(NaN === NaN)        // false
console.log(typeof NaN)         // number

console.log('mango'.length == 'avocado'.length)  // false
console.log('mango'.length != 'avocado'.length)  // true
console.log('mango'.length < 'avocado'.length)   // true
console.log('milk'.length == 'meat'.length)      // true
console.log('milk'.length != 'meat'.length)      // false
console.log('tomato'.length == 'potato'.length)  // true
console.log('python'.length > 'dragon'.length)   // false
```

נסה להבין את ההשוואות לעיל עם קצת היגיון. לזכור ללא שום היגיון עשוי להיות קשה.
JavaScript היא איכשהו סוג  של שפת תכנות. קוד JavaScript רץ ונותן לך תוצאה, אבל אלא אם כן אתה לא מבין, ייתכן שזו לא התוצאה הרצויה.

ככלל אצבע, אם ערך אינו נכון עם == הוא לא יהיה שווה ל-===. שימוש ב=== בטוח יותר משימוש ב==. ב-[קישור](https://dorey.github.io/JavaScript-Equality-Table/) יש רשימה ממצה של השוואה בין סוגי נתונים.

### אופרוטרים לוגיים

הסמלים הבאים הם האופרטורים הלוגיים הנפוצים:
&&(גם) , ||(או) ו-!(שלילה).
האופרטור && מקבל אמת רק אם שני האופרנדים נכונים.
ה || האופרטור מקבל אמת כל אחד מהאופרנד הוא אמת.
ה ! האופרטור שולל אמת ל-false ו-false ל-true.

```js
// && דוגמה לאופרטור (and)גם 

const check = 4 > 3 && 10 > 5         // true && true -> true
const check = 4 > 3 && 10 < 5         // true && false -> false
const check = 4 < 3 && 10 < 5         // false && false -> false

// || pipe or operator, example

const check = 4 > 3 || 10 > 5         // true  || true -> true
const check = 4 > 3 || 10 < 5         // true  || false -> true
const check = 4 < 3 || 10 < 5         // false || false -> false

//! Negation examples

let check = 4 > 3                     // true
let check = !(4 > 3)                  //  false
let isLightOn = true
let isLightOff = !isLightOn           // false
let isMarried = !false                // true
```

### אופורטור +

ב-JavaScript אנו משתמשים באופרטור + כדי להגדיל ערך המאוחסן במשתנה. התוספת יכולה להיות תוספת לפני או אחרי. הבה נראה כל אחד מהם:

1. תוספת מראש

```js
let count = 0
console.log(++count)        // 1
console.log(count)          // 1
```

1. לאחר ההגדלה

```js
let count = 0
console.log(count++)        // 0
console.log(count)          // 1
```

אנחנו משתמשים ברוב הזמן לאחר ההגדלה. לפחות אתה צריך לזכור כיצד להשתמש באופרטור שלאחר ההגדלה.

### אופורטור -


ב-JavaScript אנו משתמשים באופרטור ה- כדי להקטין ערך המאוחסן במשתנה. ההפחתה יכולה להיות לפני או אחרי ההפחתה. הבה נראה כל אחד מהם:

1. הפחתה מראש

```js
let count = 0
console.log(--count) // -1
console.log(count)  // -1
```

2. לאחר ההפחתה

```js
let count = 0
console.log(count--) // 0
console.log(count)   // -1
```

### Ternary Operators

Ternary operator allows to write a condition.
Another way to write conditionals is using ternary operators. Look at the following examples:

```js
let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
isRaining = false

isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
```

```sh
You need a rain coat.
No need for a rain coat.
```

```js
let number = 5
number > 0
  ? console.log(`${number} is a positive number`)
  : console.log(`${number} is a negative number`)
number = -5

number > 0
  ? console.log(`${number} is a positive number`)
  : console.log(`${number} is a negative number`)
```

```sh
5 is a positive number
-5 is a negative number
```

### Operator Precedence

I would like to recommend you to read about operator precedence from this [link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)

## Window Methods

### Window alert() method

As you have seen at very beginning alert() method displays an alert box with a specified message and an OK button. It is a builtin method and it takes on argument.

```js
alert(message)
```

```js
alert('Welcome to 30DaysOfJavaScript')
```

Do not use too much alert because it is destructing and annoying, use it just to test.

### Window prompt() method

The window prompt methods display a prompt box with an input on your browser to take input values and the input data can be stored in a variable. The prompt() method takes two arguments. The second argument is optional.

```js
prompt('required text', 'optional text')
```

```js
let number = prompt('Enter number', 'number goes here')
console.log(number)
```

### Window confirm() method

The confirm() method displays a dialog box with a specified message, along with an OK and a Cancel button.
A confirm box is often used to ask permission from a user to execute something. Window confirm() takes a string as an argument.
Clicking the OK yields true value, whereas clicking the Cancel button yields false value.

```js
const agree = confirm('Are you sure you like to delete? ')
console.log(agree) // result will be true or false based on what you click on the dialog box
```

These are not all the window methods we will have a separate section to go deep into window methods.

## אובייקט תאריך

זמן הוא דבר חשוב. אנחנו אוהבים לדעת את השעה שבה פעילות או אירוע מסוים. ב-JavaScript השעה והתאריך הנוכחיים נוצרים באמצעות אוביקט של Date של JavaScript. האובייקט שאנו יוצרים באמצעות אובייקט Date מספק מתודות רבות לעבודה עם תאריך ושעה. המתודות בהן אנו משתמשים כדי לקבל מידע על תאריך ושעה מאובייקט התאריך מתחילים במילה _get_ מכיוון שהיא מספקת את המידע.
_getFullYear(), getMonth(), getDate(), getDay(), getHours(), getMinutes, getSeconds(), getMilliseconds(), getTime(), getDay()_

![Date time Object](../images/date_time_object.png)

### יצירת אובייקט זמן

ברגע שאנו יוצרים אובייקט זמן. אובייקט הזמן יספק מידע על הזמן. הבה ניצור אובייקט זמן

```js
const now = new Date()
console.log(now) // Sat Jan 04 2020 00:56:41 GMT+0200 (שעון תקן מזרח אירופי)
```

יצרנו אובייקט זמן ונוכל לגשת לכל מידע על תאריך שעה מהאובייקט באמצעות המתודות get שהזכרנו בטבלה.

### קבלת שנה 

בואו נחלץ או נקבל את השנה המלאה מאובייקט זמן.

```js
const now = new Date()
console.log(now.getFullYear()) // 2022
```

### קבלת חדש

בואו נחלץ או נקבל את החודש מאובייקט זמן.

```js
const now = new Date()
console.log(now.getMonth()) // 0, כי החודש הוא ינואר, חודשים (0-11)
```

### קבלת תאריך

בואו נחלץ או נקבל את תאריך החודש מאובייקט זמן.

```js
const now = new Date()
console.log(now.getDate()) //4, כי היום בחודש הוא הרביעי, ימים (1-31)
```

### קבלת יום

בואו נחלץ או נקבל את היום בשבוע מאובייקט זמן.

```js
const now = new Date()
console.log(now.getDay()) // 6, כי היום הוא שבת שהוא היום השביעי
//  יום ראשון הוא 0, יום שני הוא 1 ושבת הוא 6
// קבלת יום השבוע כמספר (0-6)
```

### קבלת שעה

בואו נחלץ או נקבל את השעות מאובייקט זמן.

```js
const now = new Date()
console.log(now.getHours()) // 0, כי השעה היא 00:56:41
```

### קבלת דקות

Let's extract or get the minutes from a time object.

```js
const now = new Date()
console.log(now.getMinutes()) // 56, כי השעה היא 00:56:41
```

### קבלת שניות

בואו נחלץ או נקבל את השניות מאובייקט זמן.

```js
const now = new Date()
console.log(now.getSeconds()) // 41, כי השעה היא 00:56:41
```

### קבלת זמן

שיטה זו נותנת זמן באלפיות שניות החל מה-1 בינואר 1970. היא ידועה גם כזמן יוניקס. אנו יכולים לקבל את זמן יוניקס בשתי דרכים:

1. שימוש ב _getTime()_

```js
const now = new Date() //
console.log(now.getTime()) // 1578092201341, זה מספר השניות שעברו מ-1 בינואר 1970 עד 4 בינואר 2020 00:56:41
```

1. שימוש ב _Date.now()_

```js
const allSeconds = Date.now() //
console.log(allSeconds) // 1578092201341, זה מספר השניות שעברו מ-1 בינואר 1970 עד 4 בינואר 2020 00:56:41

const timeInSeconds = new Date().getTime()
console.log(allSeconds == timeInSeconds) // true
```

תן לנו לעצב את הערכים האלה לפורמט זמן קריא אנושי.
**דוגמה:**

```js
const now = new Date()
const year = now.getFullYear() // מחזיר שנה
const month = now.getMonth() + 1 // מחזיר חודש(0 - 11)
const date = now.getDate() // מחזיר יום החודש (1 - 31)
const hours = now.getHours() // מחזיר שעה (0 - 23)
const minutes = now.getMinutes() // מחזיר דקה (0 -59)

console.log(`${date}/${month}/${year} ${hours}:${minutes}`) // 4/1/2020 0:56
```

🌕 יש לך אנרגיה חסרת גבולות. זה עתה סיימת את אתגרי היום השלישי ואת שלושה צעדים ראש בראש בדרכך לגדולה. עכשיו תעשה כמה תרגילים למוח שלכך ולשרירים שלך.

## 💻 Day 3: Exercises

### Exercises: Level 1

1. Declare firstName, lastName, country, city, age, isMarried, year variable and assign value to it and use the typeof operator to check different data types.
2. Check if type of '10' is equal to 10
3. Check if parseInt('9.8') is equal to 10
4. Boolean value is either true or false.
   1. Write three JavaScript statement which provide truthy value.
   2. Write three JavaScript statement which provide falsy value.

5. Figure out the result of the following comparison expression first without using console.log(). After you decide the result confirm it using console.log()
   1. 4 > 3
   2. 4 >= 3
   3. 4 < 3
   4. 4 <= 3
   5. 4 == 4
   6. 4 === 4
   7. 4 != 4
   8. 4 !== 4
   9. 4 != '4'
   10. 4 == '4'
   11. 4 === '4'
   12. Find the length of python and jargon and make a falsy comparison statement.

6. Figure out the result of the following expressions first without using console.log(). After you decide the result confirm it by using console.log()
   1. 4 > 3 && 10 < 12
   2. 4 > 3 && 10 > 12
   3. 4 > 3 || 10 < 12
   4. 4 > 3 || 10 > 12
   5. !(4 > 3)
   6. !(4 < 3)
   7. !(false)
   8. !(4 > 3 && 10 < 12)
   9. !(4 > 3 && 10 > 12)
   10. !(4 === '4')
   11. There is no 'on' in both dragon and python

7. Use the Date object to do the following activities
   1. What is the year today?
   2. What is the month today as a number?
   3. What is the date today?
   4. What is the day today as a number?
   5. What is the hours now?
   6. What is the minutes now?
   7. Find out the numbers of seconds elapsed from January 1, 1970 to now.

### Exercises: Level 2

1. Write a script that prompt the user to enter base and height of the triangle and calculate an area of a triangle (area = 0.5 x b x h).

   ```sh
   Enter base: 20
   Enter height: 10
   The area of the triangle is 100
   ```

1. Write a script that prompt the user to enter side a, side b, and side c of the triangle and and calculate the perimeter of triangle (perimeter = a + b + c)

   ```sh
   Enter side a: 5
   Enter side b: 4
   Enter side c: 3
   The perimeter of the triangle is 12
   ```

1. Get length and width using prompt and calculate an area of rectangle (area = length x width and the perimeter of rectangle (perimeter = 2 x (length + width))
1. Get radius using prompt and calculate the area of a circle (area = pi x r x r) and circumference of a circle(c = 2 x pi x r) where pi = 3.14.
1. Calculate the slope, x-intercept and y-intercept of y = 2x -2
1. Slope is m = (y<sub>2</sub>-y<sub>1</sub>)/(x<sub>2</sub>-x<sub>1</sub>). Find the slope between point (2, 2) and point(6,10)
1. Compare the slope of above two questions.
1. Calculate the value of y (y = x<sup>2</sup> + 6x + 9). Try to use different x values and figure out at what x value y is 0.
1. Writ a script that prompt a user to enter hours and rate per hour. Calculate pay of the person?

    ```sh
    Enter hours: 40
    Enter rate per hour: 28
    Your weekly earning is 1120
    ```

1. If the length of your name is greater than 7 say, your name is long else say your name is short.
1. Compare your first name length and your family name length and you should get this output.

    ```js
    let firstName = 'Asabeneh'
    let lastName = 'Yetayeh'
    ```

    ```sh
    Your first name, Asabeneh is longer than your family name, Yetayeh
    ```

1. Declare two variables _myAge_ and _yourAge_ and assign them initial values and myAge and yourAge.

   ```js
   let myAge = 250
   let yourAge = 25
   ```

   ```sh
   I am 225 years older than you.
   ```

1. Using prompt get the year the user was born and if the user is 18 or above allow the user to drive if not tell the user to wait a certain amount of years.

    ```sh

    Enter birth year: 1995
    You are 25. You are old enough to drive

    Enter birth year: 2005
    You are 15. You will be allowed to drive after 3 years.
    ```

1. Write a script that prompt the user to enter number of years. Calculate the number of seconds a person can live. Assume some one lives just hundred years

   ```sh
   Enter number of years you live: 100
   You lived 3153600000 seconds.
   ```

1. Create a human readable time format using the Date time object
   1. YYYY-MM-DD HH:mm
   2. DD-MM-YYYY HH:mm
   3. DD/MM/YYYY HH:mm

### Exercises: Level 3

1. Create a human readable time format using the Date time object. The hour and the minute should be all the time two digits(7 hours should be 07 and 5 minutes should be 05 )
   1. YYY-MM-DD HH:mm eg. 20120-01-02 07:05

[<< Day 2](../02_Day_Data_types/02_day_data_types.md) | [Day 4 >>](../04_Day_Conditionals/04_day_conditionals.md)
