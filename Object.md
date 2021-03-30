# JavaScript - Object

JavaScript: 使用原型基礎(prototype-based), other programs use 類別基礎(class-based)。

Object Memeber : 屬性(property.prop),"方法(method)"

const emptyObject = {}

```javascript=
const player = {
    fullName: 'Ichiro',
    age: 23,
    gender: 'boy',
    hairColor: 'brown',
}

player.age = 24
```


## Class (類別)
類別(Class)先定義好物件的整體結構藍圖(blue print)，然後再用這個類別定義，來產生相同結構的多個的物件實例

```javascript=
class Player {
    constructor(fullName, age, gender, hairColor) {
        this.fullName = fullName
        this.age = age
        this.gender = gender
        this.hairColor = hairColor
    }

    toString() {
        return 'Name: '+this.fullName+', Age:'+this.age
    }
}

const inori = new Player('Inori', 16, 'girl', 'pink')
console.log(inori.toString()) //Name: Inori 16
console.log(inori.fullName) // Inori

const tsugumi = new Player('Tsugumi', 14, 'girl', 'purple')
console.log(tsugumi.toString())//Name: Tsugumi 14
```

## Constructor (建構式)
一個 class 只能有一個稱為 constructor 的特殊物件。
The constructor method is a special method of a class for creating and initializing an object of that class.

`constructor([arguments]) { ... }`


```javascript=
class Polygon {
  constructor() {
    this.name = 'Polygon';
  }
}

const poly1 = new Polygon();

console.log(poly1.name);
// expected output: "Polygon"
```


## Static (靜態)#
JavaScript中只有靜態方法，沒有靜態屬性。
```javascript=
class Student {
    constructor(id, firstName, lastName) {
        this.id = id
        this.firstName = firstName
        this.lastName = lastName

        //這裡呼叫靜態方法，每次建構出一個學生實體就執行一次
        Student._countStudent()
    }

    //靜態方法的定義
    static _countStudent(){
      if(this._numOfStudents === undefined) {
          this._numOfStudents = 1
      } else {
          this._numOfStudents++
      }
    }

    //用getter與靜態方法取出目前的學生數量
    static get numOfStudents(){
      return this._numOfStudents
    }

}

const aStudent = new Student(11, 'Eddy', 'Chang')
console.log(Student.numOfStudents) //1

const bStudent = new Student(22, 'Ed', 'Lu')
console.log(Student.numOfStudents) //2

const cStudent = new Student(33, 'Horward', 'Liu')
console.log(Student.numOfStudents) //3
```


## Extend (繼承)
`class ChildClass extends ParentClass { ... }`
Used in class declarations or class expressions to create a class that is a child of another class.

```javascript=
class DateFormatter extends Date {

  getFormattedDate() {
    const months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun',
      'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'];
    return `${this.getDate()}-${months[this.getMonth()]}-${this.getFullYear()}`;
  }

}

console.log(new DateFormatter('August 19, 1975 23:15:30').getFormattedDate());
// expected output: "19-Aug-1975"

```