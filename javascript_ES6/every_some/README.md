# Every & Some

## Every 
จะต้องแมทในทุกๆตัวใน array ถึงจะรีเทิร์นค่าเป็น true

## Some 
มีค่าใดค่าหนึ่งแมทใน array ก็จะรีเทิร์น true แต่ถ้าไม่มีค่าที่แมทเลย ถึงจะรีเทิร์น false

```javascript
const members = [ 
   {name: "Eve", age: 24}, 
   {name: "Adam", age: 48}, 
   {name: "Chris", age: 18}, 
   {name: "Danny", age: 30}
]

const everyResult = members.every((member) => {
  return member.age > 25
})
console.log(everyResult)

const someResult = members.some((member) => {
  return member.age > 25
})
console.log(someResult)
```

## ผลลัพธ์
```javascript
false
true
```