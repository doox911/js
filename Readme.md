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
const toString = {}.toString

console.log(toString.call(undefined));
console.log(toString.call(null));
console.log(toString.call(0));
console.log(toString.call('undefined'));
console.log(toString.call(Symbol(11)));
console.log(toString.call((() => {})));
console.log(toString.call([]));
console.log(toString.call(true));

function typeIs(type) {
  return {}.toString.call(type).replace('\]', '').split(' ')[1];
}
```

