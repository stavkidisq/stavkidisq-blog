### Типы данных в JavaScript.
В языке JavaScript имеется два типа данных. А именно: *примитивы* и *объекты*.
#### Примитивы
```js
let num = 123; // "number"
let str = "string"; // "string"
let bool = true; // "boolean"
let nullable = null; // "object"
let undef = undefined; // "undefined"

let obj = {}; // "object"
let newObj = new Object(); // "object"
let dateObj = new Date("December 25, 1995 13:30:00"); // return a string, but "object"
let newNumber = new Number("123"); // return a number, but "object"
let func = function() {}; // "function"
let aFunc = () => {}; // "function"
let nan = NaN; // "number"

// Разные виды записи чисел
let num2_0 = 1e3;
let num2_1 = 0b0000111011;
let num2_2 = 0o1750;
let num2_3 = 0x3E8;
```
#### Преобразования типов.
```js
const res3_0 = 2 + 2; // "number"
const res3_1 = 2 + "2"; // "string"
const res3_2 = 2 + "" + 2; // "string"
const res3_3 = 2 + +"2"; // Плюс в плотную к строке = число => "number"
```

Все, что внутри языка HTML - это строки!

```js
const res3_4 = !!" "; // true
const res3_5 = !!""; // false
const res3_6 = !!4; // true
const res3_7 = !!0; // false

const res3_8 = false + "1"; // "false1"
const res3_9 = true + 1; // 2, т.к. true -> 1
const res3_10 = !!{}; // true
const res3_11 = !!null; // false
const res3_12 = 1 * {}; //NaN
const res3_13 = !!NaN // false
```

#### Функции
Есть два способа задания функции: `function declaration` и `function expression`.
```js
// Function declaraion
let res6_0 = 0;
declaredFunc(1); // Сработает
function declaredFunc(arg6_0){
  res6_0 + arguments[0];
}
```
```js
// Function expression
let res6_1 = 0;
expressedFunc(2); // Не сработает
const expressedFunc = function(arg6_1){
  res6_1 += arg6_1;
  let res = arg6_1;
  return res;
}
```

Также можно создать стрелочную функцию: 
```js
//Function expression
let res6_2 = 0;
arrowFunc(2); // Не сработает
let arrowFunc = (arg6_2) => {
  return res6_2 + arg6_2;
}
```

Также в параметры функции можно ничего не вводить:
```js
sum(1, 2); // => 3
function sum(){
  return arguments[0] + arguments[1];
}
```
Роль аргументов функции в данно слкчае играет массив `arguments`.
