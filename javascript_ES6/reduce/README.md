# Reduce

Reduce จะแตกต่างจาก map กับ filter ตรงที่มันจะมีการเก็บค่า current เอาไว้ และสามารถทำมาใช้ทำงานกับ array ในตัวถัดๆไปได้อีกด้วย
```javascript
const items = [1,2,3,4,5]

const result = items.reduce((item, currentItem) => {
	return item + currentItem
}, 0)

console.log(result)
```

## ผลลัพธ์
```
15
```