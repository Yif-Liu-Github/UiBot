# UiBot
Uibot learning


## Day 01
### 变量赋值（可赋值立即数值，表达式，函数返回值等）
### 变量名不区分大小写，类型可动态改变
Dim 变量名=值, 变量名=值  
Const 常量名=值, 常量名=值
函数型：函数型的值只能是已经定义好的函数  
空值型：空值型的值总是Null，不区分大小写  
```
dim a_1=1,a_b=&H2   
//定义两个数值变量，十六进制数字前缀&H
Const c=3.333,tr=True   
//定义两个常量，浮点型，布尔型
dim s1='字符串',s2="\'\"字符串"   
//定义两个字符串,此处s2中用了转义\t 代表制表符，用 \n 代表换行，用 \’ 代表单引号，用 \” 代表双引号，用 \ 代表反斜杠本身
dim s3='''1!2@3#4$5%6^7&8*9(0)
~`{}|:"<>   ?[]\\;',./'''   
\\可以用前后各三个单引号来（’’’）表示一个字符串，这种字符串被称为长字符串。在长字符串中，可以直接写回车符、单引号和双引号，无需用\n，\’或者\”
dim ar=[1,'a',3.333,[&hB,true,'\'']]    
\\定义数组
dim dic={"num":1,"arr":[1,'a',true]}    
\\定义字典{ 名字1:值1, 名字2:值2, 名字3:值3 }其中 名字 只能是字符串，值可以是任意类型的表达式
TracePrint(a_1,a_b,c,tr,s1,s2,s3,ar,dic["arr"][1])   
\\1 2 3.333 true "字符串" "'"字符串" "1!2@3#4$5%6^7&8*9(0) ~`{}|:"<> ?[]\;',./" [ 1, "a", 3.3330000000000002, [ 11, true, "'" ] ] "a"
```


### 条件分支（以If 开头，以End If结尾）
```
if a=3//判断条件是否成立
TracePrint(a)
elseif a=2
TracePrint(a)
elseif a=1
TracePrint(a) 
Else
TracePrint(0)
End If//结束判断
```

### 计次循环（以for 开头，以next结尾，step控制步长）
```
for i=1 to 10 step 2//从1到10循环，每次增加1
TracePrint(i) //执行语句
Next//进入下个循环
```
