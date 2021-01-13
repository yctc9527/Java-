```java
字符串StringBuilder
String和StringBuilder的区别：
String具有不可变性，而StringBuilder不具备，当频繁操作字符串时使用StringBuilder
StringBuilder和StringBuffer：
二者基本相似，StringBuffer是线程安全的，StringBuilder则没有所以性能略高
StringBuilder构造方法
StringBuilder()不带参数:创建一个空串，默认定义一个16个字符大小的容量
StringBuilder(CharSequence seq)接口作为参数等同于String类使用
StringBuilder(int capcity)：这是一个指定容量的参数
StringBuilder(String str)
成员方法
append（）在字符串的末尾增加数据
charAt（）在一个位置插入内容
delete（）删除字符
insert（）插入
replace（）替换
substring（）求子串
toString（）       
```

StringBuilder常用方法

- append(String str)/append(Char c)：字符串连接

  ```java
  System.out.println("StringBuilder:"+strB.append("ch").append("111").append('c'));
  //return "StringBuilder:ch111c"
  12
  ```

- toString()：返回一个与构建起或缓冲器内容相同的字符串

  ```java
  System.out.println("String:"+strB.toString());
  //return "String:ch111c"
  12
  ```

- 3、appendcodePoint(int cp)：追加一个代码点，并将其转换为一个或两个代码单元并返回this

  ```java
  System.out.println("StringBuilder.appendCodePoint:"+strB.appendCodePoint(2));
  //return "StringBuilder.appendCodePoint:ch111c"
  12
  ```

- 4、setCharAt(int i, char c)：将第 i 个代码单元设置为 c（可以理解为替换）

  ```java
  strB.setCharAt(2, 'd');
  System.out.println("StringBuilder.setCharAt:" + strB);
  //return "StringBuilder.setCharAt:chd11c"
  123
  ```

- 5、insert(int offset, String str)/insert(int offset, Char c)：在指定位置之前插入字符(串)

  ```java
  System.out.println("StringBuilder.insertString:"+ strB.insert(2, "LS"));
  //return "StringBuilder.insertString:chLSd11c"
  12
  ```

- 6、delete(int startIndex,int endIndex)：删除起始位置（含）到结尾位置（不含）之间的字符串

  ```java
  System.out.println("StringBuilder.delete:"+ strB.delete(2, 4));
  //return "StringBuilder.delete:chSd11c"
  ```