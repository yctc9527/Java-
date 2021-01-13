# 1.String的构造方法

### 1）String(String original):把字符串数据封装成字符串对象

### 2）String(char[] value):把字符数组的数据封装成字符串对象

### 3）String(char[] value, int index, int count):把字符数组中的一部分数据封装成字符串对象

# 2.String类的获取功能：

### 1）length():获取字符串的长度，其实也就是字符个数

```java
String str = "adsfaxsdfas沙发上案发地方";
System.out.println(str.length());
```

运行结果：
18

### 2）charAt(int index):获取指定索引处的字符

```java
String str = "adsfaxsdfas沙发上案发地方";
		
char[] c = {'a','d','s','f','a'};
System.out.println(str.charAt(12));
```

运行结果：
发

### 3）indexOf(String str):获取str在字符串对象中第一次出现的索引

```java
String str = "adsfaxsdfas沙发上案发地方";
System.out.println(str.indexOf('a');
```

运行结果：
9

### 4）substring(int start):从start开始截取字符串

```java
String str = "adsfaxsdfas沙发上案发地方";
System.out.println(str.substring(1));
```

运行结果：
dsfaxsdfas沙发上发地方

### 5）String substring(int start,int end):从start开始，到end结束截取字符串。包括start，不包括end

```java
String str = "adsfaxsdfas沙发上案发地方";
System.out.println(str.substring(1, 12));
```

运行结果：
dsfaxsdfas沙

# 3.String判断功能

### 1）equals(Object obj):比较字符串的内容是否相同

```java
String str = "adsfaxsdfas沙发上案发地方";
System.out.println(str.equals("adsfaxsdfas沙发上发地方"));
System.out.println(str.equals("adsfaxsdfas"));
```

运行结果：
true
false

### 2）equalsIgnoreCase(String anotherString):比较字符串的内容是否相同,忽略大小写

```java
String str = "adsfaxsdfas沙发上案发地方";
System.out.println(str.equalsIgnoreCase("ADsfaxsdfAs沙发上发地方"));
```

运行结果：
true

### 3）startsWith(String prefix):判断字符串对象是否以指定的字符开头（区分大小写）

```java
String str = "adsfaxsdfas沙发上案发地方";
System.out.println(str.startsWith("a"));
System.out.println(str.startsWith("A"));
```

运行结果：
true
false

### 4）startsWith(String prefix,int toffset)：判断字符串对象是否以指定的字符开头，参数toffset为指定从哪个下标开始

```java
String str = "adsfaxsdfas沙发上案发地方";
System.out.println(str.startsWith("f", 3));
System.out.println(str.startsWith("f", 4));
```

运行结果：
true
false

### 5）endsWith(String str):判断字符串对象是否以指定的字符结尾

```java
String str = "adsfaxsdfas沙发上案发地方";
System.out.println(str.endsWith("x"));
System.out.println(str.endsWith("方"));
```

运行结果：
false
true

### 6）isEmpty()：判断指定字符串是否为空

# 4.String类中的转化方法：

### 1）toCharArray():把字符串转换为字符数组

```java
public static void main(String[] args) {
		String str = "adsfaxsdfas沙发上发地方";
		char arr[] = str.toCharArray();
		printArray(arr);
}
public static void printArray(char a[]) {
		
		for(int i=0;i<a.length;i++) {
			System.out.print(a[i]+"--");
		}
}
```

运行结果：
a–d--s–f--a–x--s–d--f–a--s–沙--发–上--发–地--方–

### 2）toLowerCase():把字符串转换为小写字符串

```java
String str1 = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
System.out.println(str1.toLowerCase());
```

运行结果：
abcdefghijklmnopqrstuvwxyz

### 3）toUpperCase():把字符串转换为大写字符串

```java
String str1 = "abcdefghijklmnopqrstuvwxyz";
System.out.println(str2.toUpperCase());
```

运行结果：
ABCDEFGHIJKLMNOPQRSTUVWXYZ

# 5.其他常用方法

### 1）trim()：去除字符串两端空格

```java
String str3 = "    a  c  e x u a n x u a n    ";
System.out.println(str3.trim());
System.out.println(str3);

运行结果：
a  c  e x u a n x u a n
    a  c  e x u a n x u a n
```

### 2）split():去除字符串中指定的的字符，然后返回一个新的字符串

```java
public static void main(String[] args) {
		
		String str = "adsfaxsdfas沙发上发地方";
		String array[] = str.split("a");
		printString(array);
}
public static void printString(String a[]) {
		for(int i=0;i<a.length;i++) {
			System.out.print(a[i]);
		}
}
```

运行结果：
dsfxsdfs沙发上发地方

### 3）subSequence(int beginIndex,int endIndex )：截取字符串中指定位置的字符组成一个新的字符串

```java
String str = "adsfaxsdfas沙发上发地方";
System.out.println(str.subSequence(1, 10));
```

运行结果：
dsfaxsdfa

### 4）replace(char oldChar, char newChar)：将指定字符替换成另一个指定的字符

```java
String str = "adsfaxsdfas沙发上发地方";
System.out.println(str.replace('a', 's'));
```

运行结果：
sdsfsxsdfss沙发上发地方

### 5）replaceAll(String regex,String replasement)：用新的内容替换全部旧内容

```java
String str4 = "Hello,world!";
System.out.println(str4.replaceAll("l", "&"));
```

运行结果：
He&&o,wor&d!

### 6）replaceFirst(String regex,String replacement)：替换首个满足条件的内容

```java
String str = "adsfaxsdfas沙发上发地方";
System.out.println(str.replaceFirst("沙", "璇"));
```

运行结果：
adsfaxsdfas璇发上发地方

### 7）lastIndexOf(String str)：返回指定字符出现的最后一次的下标

```java
String str4 = "Hello,world!";
System.out.println(str4.lastIndexOf("l"));
```

运行结果：
9

### 8）contains(CharSequence s)：查看字符串中是都含有指定字符

```java
String str4 = "Hello,world!";
System.out.println(str4.contains("l"));
```

运行结果：
true

### 9）concat(String str)：在原有的字符串的基础上加上指定字符串

```java
String str5 = "dr";
System.out.println(str5.concat("eam"));
```

运行结果：
dream