# JavaScript - Array

## **Array:**
- no fixed length and type
- the value could be changed (reference)
- not use `new` to initialize the size



```javascript=
# Create an Array

let fruit = ['Apple', 'Banana','Orange']
console.log(fruit.length)//3

const a = []
const b = [1, 2, 3]

console.log(a.length) //0

a[0] = 1
a[1] = 2
a[2] = 3
a[2] = 5 //change the value

console.log(typeof aArray) // object
console.log(aArray) // [1,2,5]
console.log(aArray.length) //3
console.log(aArray[3]) //undefined
```


## 多維陣列
```javascript=
const magicMatrix = [
      [2, 9, 4],
      [7, 5, 3],
      [6, 1, 8]
]

magicMatrix[2][1] //7
```

## Holey/Sparse Arrays
```javascript=
const aArray = []
aArray[0] = 1
aArray[6] = 3

const bArray = [1, , 3]
```






```javascript=
# Access an Array item using index

let first = fruit[0]
//Apple

let last = fruit[fruit.length -1]
//Orange
```

## Copy Array
```javascript=

```


```javascript=
const a =[]
```

## length 
```javascript=
const aArray = [1, undefined, '123']
console.log();

const sArray =['apple','lemon','mango','grape']
sArray.length=2
console.log(sArray)

#["apple","lemon"]
```