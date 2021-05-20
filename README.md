Гайд по стилю кода JavaScript

## Содержание:
1. __[Именование переменных](#Именование-переменных)__ 
2. __[Объявление переменных](#Объявление-переменных)__
3. __[Немедленно вызываемые функции IIFE](#Немедленно-вызываемые-функции-IIFE)__
4. __[Создание массивов](#Создание-массивов)__
5. __[Создание объектов](#Создание-объектов)__
6. __[Название ключей в объектах](#Название-ключей-в-объектах)__
7. __[Отступы](#Отступы)__
8. __[Точка с зяпятой](#Точка-с-зяпятой)__
9. __[Именование классов](#Именование-классов)__
10. __[Switch case](#Switch-case)__

## Именование переменных
Имя переменной должно максимально отражать ее суть.Избегай однобуквенных названий. Используйте слова английского языка. Для длинных названи используй camelCase.
&nbsp; 

❌ 
```javascript
let q;
let polzovatel;
const NaMeUser;
```

✅
```javascript
let question;
let user;
const nameUser;
```

## Объявление переменных
Для объявения переменных используй let и const. Используй ключевые слова для объявления каждой переменной. Если переменная не переназначается то const, и наоборот.
&nbsp; 

❌ 
```javascript
const animal = 'dog',
    isCat = true,
    getName();
    
var count = 1;
if (true) {
  count++;
}
```

✅
```javascript
const animal = 'dog';
const isCat = true;
let name = getName();

let count = 1;
if (true) {
  count++;
}
```
## Немедленно вызываемые функции IIFE
Оборачивай в скобки немедленно вызывамые функции.
&nbsp; 

❌ 
```javascript
 const name = function showName() {
  console.log('Настя');
}();
```

✅
```javascript
const name = (function showName() {
  console.log('Настя');
})();
```
## Создание массивов
Для создания массива используй квадратные скобки []. Не используй new Arrary().
&nbsp; 

❌ 
```javascript
 let items = new Array();
```

✅
```javascript
let items = [];
```
## Создание объектов
Для создания объекта используй фигурные скобки {}. Не используй new Object().
&nbsp; 

❌ 
```javascript
 let user = new Object();
```

✅
```javascript
let user = {};
```
## Название ключей в объектах
Не дублируй названия ключей в объектах.
&nbsp; 

❌ 
```javascript
 let user = {
   "name": 'Настя',
   name: 'Анастасия'
 };
```

✅
```javascript
let user = {
   name: 'Настя',
   fullName: 'Анастасия'
 };
```
## Отступы
Используй отступ в два пробела для каждого уровня вложенности.
&nbsp; 

❌ 
```javascript
function getUserName(url) {
let allUrl = url.split('=');
let name = allUrl[1];
      if (!name) {
 name = 'defunkt';
  }
 return name;
}
```

✅
```javascript
function getUserName(url) {
  let allUrl = url.split('=');
  let name = allUrl[1];
  if (!name) {
    name = 'defunkt';
  }

  return name;
}
```
## Точка с запятой
Всегда ставьте точку с запятой в конце выражения.
&nbsp; 

❌ 
```javascript
function getFullName(name, surname) {
  let fullName = `${name} ${surname}`
  return fullName
}
```

✅
```javascript
function getFullName(name, surname) {
  let fullName = `${name} ${surname}`;
  return fullName;
}
```
## Именование классов
Для названия классов действуют те же правила, что и для названия переменных, но следует писать название класса с заглавной буквы.
&nbsp; 

❌ 
```javascript
function user(options) {
  this.name = options.name;
}

let userAdmin = new user();
```

✅
```javascript
function User(options) {
  this.name = options.name;
}

let userAdmin = new User();
```
## Switch case
Не повторяй условия в конструкции switch case.
&nbsp; 

❌ 
```javascript
let name = 'Admin';

switch (name) {
  case 'Anna':
    console.log('Ты не админ!');
    break;
  case 'Admin':
    console.log('А вот ты админ!');
    break;
  case 'Anna':
    console.log('Не нужно повторять условия!');
    break;         
  default:
    console.log('Попробуй еще раз');
    break;
}
```

✅
```javascript
let name = 'Admin';

switch (name) {
  case 'Anna':
    console.log('Ты не админ!');
    break;
  case 'Admin':
    console.log('А вот ты админ!');
    break;        
  default:
    console.log('Попробуй еще раз');
    break;
}
```
**[⬆ Вернуться к содержанию](#Cодержание)**
