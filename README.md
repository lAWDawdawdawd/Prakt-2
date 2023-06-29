
#1

function getType(arg) { return typeof arg };
console.log(getType(10));
console.log(getType(true)); 
console.log(getType(“Ruslan”));

#2

При запуске, он выведет "a". Это связано с тем, что в этом коде оператор && возвращает первое значение, которое является true. Поскольку значение a()) не является ложным значением, оно возвращается, а затем вызывается a(), которая выводит "a". Следовательно, "с" будет иметь значение "a".
const a = () => console.log("a");
const b = () => console.log("b");
const c = a && b ? a() : b();
console.log(c);

#4

function convertArrToObj(arr) { let obj = {}; for (let i = 0; i < arr.length; i++) { obj[i] = arr[i]; } return obj; }
const arr = [1, null, 'test', undefined]; const obj = convertArrToObj(arr); console.log(obj); // { 0: 1, 1: null, 2: 'test', 3: undefined }

#5

const arr = [1, 1, 1, 'test', 'test']
function countFromArr(arr) { return arr.reduce((acc, item) => { if (acc[item]) { acc[item] += 1; } else { acc[item] = 1; } return acc }, {}) }
const res = countFromArr(arr); console.log(res); // { 1: 3, test: 2 }

#6

const arr = [{test: 1},{test: 2},{test: 3},{test: 1},{test: 1}]
function groupByField(arr, fieldName) { return arr.reduce((acc, item) => { let key = item[fieldName]; if (acc[key]) { acc[key].push(item); } else { acc[key] = [item]; } return acc }, {}) }
const res = groupByField(arr, 'test'); console.log(res); // { 1: [{test: 1}, {test: 1}, {test: 1}], 2: [{test: 2}], 3: [{test: 3}]}

#7

def plus(value, value1): return value + value1 print(plus(1,2))

#8

start promise constructor final p2 p4 p5 timeout
