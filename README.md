### 《JS 对象基本用法》
* 声明对象的两种语法
* 如何删除对象的属性
* 如何查看对象的属性
* 如何修改或增加对象的属性
* 'name' in obj和obj.hasOwnProperty('name') 的区别

1. **声明对象的两种语法**
*let声明*
规则:遵循块作用域，即使用范围不能超出{}
不能重复声明
可以赋值，也可以不赋值
必须先声明再使用，否则会报错
全局声明的let变量不会变成window的属性
for循环配合let有奇效
*const声明*
规则:几乎同let一样，但是声明一定要赋值，赋值后不能改。
2. **如何删除对象的属性**
```JavaScript
删除obj的xxx属性:
delete obj.xxx 或 delete obj['xxx']
只删除xxx的属性值:
obj.xxx = undefined
判断是否含属性名:
'xxx' in obj
判断属性名的值为undefined:
'xxx' in obj&&obj.xxx
//obj.xxx为undefined不能判断'xxx'是否为obj属性
```

3. **如何查看对象的属性**
```JavaScript
中括号语法:  obj['key']
点语法:  obj.key//key是字符串
一般语法: obj[key]//key是变量
```

4. **如何修改或增加对象的属性**
```JavaScript
obj.name='frank'//直接赋值
Object.assign(obj,{age:18,gender:'man'})//批量赋值

```


5. **'name' in obj和obj.hasOwnProperty('name') 的区别**
```JavaScript
'name' in obj
//判断是否含属性名name
obj.hasOwnProperty('name')
//判断属性name是自身属性还是共有属性


let obj = { name: 'aaa' }; 
'name' in obj // true 
'toString' in obj // true

console.log(obj.hasOwnProperty('toString')) // false
```