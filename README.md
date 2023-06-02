# ReactStudy에서 많이 사용되는 JavaScript문법들!
<br>
<h3>1. object shorthand assignment</h3>
<br>
let name = 'inhwan';<br>
let age = 26;<br>

let person = {<br>
  name,<br>
  age,<br>
};<br>
console.log(person);<br>
<br>

<h3>2.Destructuring</h2>
<br>
let person = {<br>
  name: 'inhwan',<br>
  age: 20,<br>
};<br>
<br>
let name = person.name;<br>
let age = person['age'];<br><br>
//위의 코드를 아래처럼 간략하게 코딩할 수 있음.<br><br>
let { name, age } = person;<br>
console.log(name, age);<br>
<br>
let array = [1, 2, 3, 4];<br>
let [a, b, ...rest] = array;<br>
<br>
console.log(rest);<br>

<h3>3.spread</h3><br>
let person = { name: 'inhwan', age: 26 };<br>

let person2 = { ...person, name: 'insoon' };<br>
let person3 = person; // person객체의 주소값만 복사. 즉 객체는 한아ㅣ고 그 객체를 참조하는 변수가 두 개인 셈이다.<br>
console.log(person2);<br>
console.log(person3);<br>
console.log(person === person2); // false<br>
console.log(person === person3); // true<br>
****배열에 적용했을 때****<br>
let a = [1, 2];<br>
let b = [...a, 3];<br>
console.log(b);<br>
let c = [...a, ...b];<br>
console.log(c);<br>

<h3>4.삼항 연산자</h3><br>
let person = { name: 'inhwan', age: 26 };<br>
 if (person) {<br>
   console.log(person.name);<br>
 } else {<br>
   console.log('there is no person');<br>
 }<br>

console.log(person ? person.name : 'there is no person');<br>
