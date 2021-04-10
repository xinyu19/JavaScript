# JavaScript - Variable, Const and Naming

## Variable
* A variable is a “named storage” for data. We can use variables to store goodies, visitors, and other data.
* Use `let` 
* 變數(Variable)在JavaScript語言中扮演了重要的資料(值)存放角色。在ES6標準之前，只有定義變數沒有定義常數的方式
* In older scripts, you may also find another keyword: `var` instead of `let`

## Constants
* To declare a constant (unchanging) variable, use `const`
* Constants cannot be reassigned

### 
變數中儲放的值，是暫時存放的，而在常數中的值是永久存放的，一旦給定值後就不會再改變的資料。

```javascript=
const a = 10
a = 11 // error, "a" is read-only

let b = 9
b = 1 
```


## Naming
* The name must contain only letters, digits, or the symbols $ and _.  開頭字元需要是ASCII字元(英文大小寫字元)，或是下底線(_)、錢號($)
* The first character must not be a digit. 數字不可用於開頭字元。
* 大小寫是有差異的
* 名稱不可使用JavaScript語言保留字詞。
* camelCase (小駝峰): variable, function 
`第一個單字以小寫字母開始；第二個單字的首字母大寫，例如：firstName、lastName。`
* PascalCase(巴斯卡)/CamelCase(大駝峰): class
`每一個單字的首字母都採用大寫字母，例如：FirstName、LastName`
* Stay away from abbreviations or short names 少用簡寫或自己發明縮寫
* 語意不明或對象不明 ex.isOk() 

## Comment
* 單行註解用的是雙斜線(//)
* 多行註解用的是/*...*/符號，這也稱為註解區塊(comment block)
```javascript=
//我是一個單行註解

/*
我是一個多行註解區塊
這是第二行註解
這是第三行註解
*/

```

## Symbols

#### 等號(=)
* `=` : 指定(Assignment)運算符號，也稱之為Basic Assignment，因為還有其他的指定運算符號，例如`(+=)`、`(*=)`。
* `==`: 相等(equal)，比較運算符號，用於比較兩個變數or常數的其中的值是否相等。它的反義符號是`(!=)`
* `===`: identity，比較運算符號，用於比較兩個變數or常數是否完全相等(包含類型與值)。它的反義符號是`(!==)`

#### 括號
* `()`: 小括號(Parentheses)，用於函式呼叫、包括流程敘述以及分隔運算的優先次序。
* `[]`: 中括號(Brackets)，用於陣列(Array)
* `{}`: 大括號(Braces)，用於程式敘述的區域分隔(函式、迴圈、流程條件)，另外也用於物件的字面文字(Object Literals)

#### 引號
* `""`: 雙引號(Quote),用於字串的宣告
* `''`: 單引號(Single Quote)，在用於字串的宣告

#### 算術運算符
* `+`: addition
* `-`: subtraction
* `*`: multiplication
* `/`: division
* `%`: Remainder
* `++`: Increment
* `--`: Decrement
* `+`: Unary plus,用於將其它類型的值強制轉換為數值(Number)
* `-`: Unary negation, 用於將其它類型的值強制轉換為數值(Number)並且為負值

#### 字串運算
用在字串連接(concatenate)時使用，其他的並不能使用
* 加(+) addition
* 加法指定(+=) Addition assignment

> 註: 加號(+)這符號至少有三種用途，而字串的連接運算會比數字的加總運算還更優先，這一點要特別注意

#### 邏輯運算符
* `&&` 與: Logical AND
* `||` 或: Logical OR
* `!` 非: Logical NOT

#### 比較運算符
* `>` : Greater than
* `<` : Less than
* `>=` : Greater than or equal
* `<=` : Less than or equal

#### 其他常用符號
* `,` : 逗號(comma)
* `:` : 冒號(colon)
* `;` : 分號(semicolon)
* `.` : 句點(dot)
* `!` : 驚嘆號(exclamation mark)
* `?` : 問號(question mark)
* `_` : 下底線(underscore）
* `-` : 連接號(hyphen）
* `*` : 星號(asterisks)
