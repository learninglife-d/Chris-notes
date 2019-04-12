# Find
find จะเหมือนกับ filter แต่ว่ามันจะรีเทิร์นมาเฉพาะค่าแรกที่แมทกันเท่านั้น
```javascript
const members = [ 
   {name: "Eve", age: 24}, 
   {name: "Adam", age: 48}, 
   {name: "Chris", age: 18}, 
   {name: "Danny", age: 30}
]
const result = members.find((member) => {
  return member.age > 25
})
console.log(result)
```

## ผลลัพธ์
```json
{"name":"Adam","age":48}
```