# Arrow Function
ES6 คือ มาตรฐานของ javascript ที่นิยมในตอนนี้ ซึ่ง Arrow Function ก็เกิดขึ้นมาพร้อมกัน

## Function แบบเดิมที่เคยใช้
```javascript
var items = [1,2,3,4];
function displayItem(items) {
    for (let i = 0; i < items.length; i++) {
        console.log(items[i]);
    }
}
displayItem(items);
```

## Function แบบ Arrow Function
```javascript
const items = [1,2,3,4]
const result = items.map((item) => {
	console.log(item)  
})
}
```

## ผลลัพธ์ของทั้ง 2 ฟังก์ชัน
```
1
2
3
4
```