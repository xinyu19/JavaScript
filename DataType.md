# JavaScript - Data Type
## Number
* JavaScript的數字(Number)是64位元的浮點數，沒有int或float, 1與1.0指的是相同的資料類型與值
* Operations: *, /, +
* Special numeric values : `Infinity`, `-Infinity` and `NaN`(不是數字).
* 最大與最小值: `Number.MAX_VALUE`與`Number.MIN_VALUE`
* Binary,Octal, Hex-> Decimal :`Number()`
```javascript=
onst binaryNumber = Number('0b11') // 3
const octalNumber = Number('0o11') // 9
const hexNumber = Number('0x11')  // 17
```
* Decimal -> Binary, Octal, Hex :`.toString([radix])`
```javascript=
const decimalNumber = 125
console.log(decimalNumber.toString()) //'125'
console.log(decimalNumber.toString(2)) //'1111101'
console.log(decimalNumber.toString(8)) //'175'
console.log(decimalNumber.toString(16)) //'7d'
```
* Float -> Integer
```javascript=
const floatValue = 10.55
const intValueOne = Math.floor( floatValue ) //地板值 10
const intValueTwo = Math.ceil( floatValue ) //天花板值 11
const intValueThree = Math.round( floatValue ) //四捨五入值 11
```
* Integer -> Float
```javascript=
const myString = (3).toFixed(2) //string, 3.00
const numObj = 12345.6789
const numObjString = numObj.toFixed() //string, 12346
// toFixed如果不加傳入參數，會視為0位小數點，而且會作四捨五入
```

## String
* can use `("")` and `('')`, but noramlly use `('')` in Javascript, `("")` in HTML
* `charAt()`: 存取一個字串中的單一個字元, JavaScript中並沒有所謂的字元(Character)類型
```javascript=
const a = 'JavaScript'.charAt(2) // 'v'
const b = 'JavaScript'[2] //'v'
console.log(typeof a) //String 
```
* Escape characters (跳脫字元): 在字串中使用一些特殊用途的字元,使用反斜線符號blackslash`(\)`來進行跳脫
```javascript=
const aString = 'This is a blackslash \\ '
const bString = 'Enter a number: \n'
```
* Template strings (樣版字串): 使用重音符號backtick(\`\`), 可以多行、加入字串,嵌入變數/常數，運算，嵌入的使用(${})
```javascript=
const firstname = 'Sylvia'
console.log(`Hello ${firstName}!
Do you want some
coffee tonight?`)
//Hello Sylvia!
//Do you want some
//coffww tonight?
const x = 5
console.log(`5 + 3= ${x + 3}`)// 5+3= 8
```
* 字串串接
使用加號(`+`)或加法指定(`+=`)
```javascript=
//使用concat()串接
const aString = 'JavaScript'
const bString = aString.concat(' is a', ' script language')
console.log(bString) //JavaScript is a script language

//使用(+=)串接
let cString = 'JavaScript'
cString += ' is a'
cString += ' script language'
console.log(cString)//JavaScript is a script language

//當運算式的左邊運算元或右邊運算元，是字串類型時，則使用字串連接(concatenating)的運算，非字串類型的運算元則使用ToString(轉為字串)的轉換。
console.log( 3 + 4 + '5' )//75
console.log( 4 + 3 + '5' + 3 )//753

//轉換某個類型為字串時，直接與一個空白字串作加號(+)運算，就會變成字串類型了
const a = 6 + ''
const b = true + ''
```
* 字串長度
`length` :字串的屬性值，可以讀取出字串目前的長度(字元個數)，中文字每個字算1個長度
```javascript=
const aString = 'Hello World!'
const bString = '你好'
const aStringLength = aString.length //12
const bStringLength = bString.length //2
```

* 大寫與小寫
`toUpperCase` : change string to uppercase
`toLowerCase` : change string to lowecase
```javascript=
const aString = 'Hello World!'
const bString = aString.toUpperCase()//HELLO WORLD!
const cString = aString.toLowerCase()//hello world!
```
* 清除字串左右空白字元
`trim` : 清除字串左右(前後)空白字元
```javascript=
const aString = ' Hello World!    '
const bString = aString.trim()
```


* 子字串搜尋(索引值)
`indexOf` : 回傳目前在字串中尋找的子字串的索引值，索引值的順序是從左邊由0開始計算，一直到字串的總長度減1。如果尋找不到該子字串，則會回傳`-1`
```javascript=
const aString = 'Apple Mongo Banana'

console.log( aString.indexOf('Apple') ) // 0
console.log( aString.indexOf('Mongo') ) // 6
console.log( aString.indexOf('Honey') ) // -1
```

* 取出子字串

`substring` : 使用兩個參數，一個是要取出的子字串的開頭索引值，另一個是要取出的子字串的結束索引值
>語法: str.substring(start[, end])
```javascript=
const aString = '0123456789'
console.log(aString.substring(0, 3)) //012
console.log(aString.substring(5, 8)) //567

//以下為特殊情況
console.log(aString.substring(4, 4)) //''
console.log(aString.substring(5)) //56789
console.log(aString.substring(5, 2)) //234
console.log(aString.substring(5, 20)) //56789
console.log(aString.substring(-5, 2)) //01
console.log(aString.substring(2, -5)) //01
console.log(aString.substring(-5, -5)) //''
```
`slice` : 和substring類似，傳入參數值也是一樣的。slice是不會有值(只有空字串)回傳的
   
> 語法: str.slice(start[, end])
```javascript=
const aString = '0123456789'
console.log(aString.slice(0, 3)) //012
console.log(aString.slice(5, 8)) //567

//以下為特殊情況
console.log(aString.slice(4, 4)) //''
console.log(aString.slice(5)) //56789
console.log(aString.slice(5, 2)) //''
console.log(aString.slice(5, 20)) //56789
console.log(aString.slice(-5, 2)) //''
console.log(aString.slice(2, -5)) //234
console.log(aString.slice(-5, -5)) //''
```

`substr` :　語法: str.substr(start[, length])

```javascript=
const aString = '0123456789'
console.log(aString.substr(2,4)) //2345
console.log(aString.substr(0,8)) //01234567
```

## Boolean
`true`, `false`
>所有的JavaScript關鍵字(保留字)都是小寫的英文，像true的話，如果寫成True、 TRUE、TrUe，都是不對的寫法。
* false: 0, -0, null, false, NaN, undefined, 空白字串('')
* true: 不是false的其他情況
```javascript=
const aBool = !!0 //false
const bBool = !!'false' //true
const cBool = !!NaN //false
```
* truthy & falsy 
短路求值(Short-circuit): 經過邏輯與(&&)與邏輯或(||)的運算後，它的回傳值是 - 最後的值(Last value)

```javascript=
//邏輯或(Logical OR)(||)運算符在運算時，如果當第1個運算子為"falsy"時，則回傳第2個運算子。否則，將會回傳第1個運算子
console.log('foo' || 'bar') // 'foo'
console.log('foo' && 'bar') // 'bar'
console.log(false || 'bar') // 'bar'
console.log(false && 'bar') // 'false'
console.log( 0 || '' || 5 || 'bar') //5
console.log( 0 && '' && 5 && 'bar') //0
console.log(false || null || '' || 0 || NaN || 'Hello' || undefined) //'Hello'
console.log(null && '' && 0 && NaN && 'Hello' && undefined && false) //'null'
```


## null & undefined
空(null): 空值，代表的是沒有值的意思。
未定義(undefined): 尚未被定義類型，或也有可能是根本不存在，完全不知道是什麼。
```javascript=
null  == undefined // true
null === undefined // false
typeof null        // object
typeof undefined   // undefined
```