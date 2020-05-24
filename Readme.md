### Falsy values ###
------------------------
number `0`

BigInt `0n`

ключевое слово `null`

ключевое слово `undefined`

boolean `false`

number `NaN`

пустая строка `""` (`''` или \`\`)


### Null and Undefined ###
-------------------------

<b>undefined</b> является неожиданным отсутствием значения.

<b>null</b> — умышленным отсутствием значения.

Для сравнения на <b>undefined</b> можно использовать `void`, так как `void` нельзя переопределить.

### Корректная проверка на типы данных ###

```javascript
function typeIs(type) {
  return {}.toString.call(type).replace('\]', '').split(' ')[1];
}

console.log(typeIs(undefined));
console.log(typeIs(null));
console.log(typeIs(0));
console.log(typeIs('undefined'));
console.log(typeIs(Symbol(11)));
console.log(typeIs((() => {})));
console.log(typeIs([]));
console.log(typeIs(true));

function typeIs(type) {
  return {}.toString.call(type).replace('\]', '').split(' ')[1];
}
```

