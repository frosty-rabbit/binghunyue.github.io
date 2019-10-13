###### 字符串方法

1. charAt(): 返回指定位置的字符串（从0开始算起）

   ```javascript
   var str = 'abc';
   var str1 = str.charAt(1);
   document.write(str1);			//输出b
   ```

2. indexOf(): 返回字符在字符串中首次出现的位置（如果没有则返回-1）

   ```javascript
   var str = 'abcb';
   var str1 = str.indexOf('b');
   document.write(str1);			//输出1
   ```

3. lastIndexOf(): 返回字符在字符串中“最后一次出现的位置”

   ```javascript
   var str = 'abcb';
   var str1 = str.lastIndexOf('b');
   document.write(str1);			//输出3
   ```

4. replace(): 替换，将字符串的部分内容替换为另外的内容

   ```javascript
   var str = 'abc';
   var str1 = str.replace('a','1');
   document.write(str1);			//输出1bc
   ```

5. slice(): 截取 （如果是负数则从后向前截取）

   ```javascript
   var str = 'abcdefg';
   var str1 = str.slice(1,5);
   document.write(str1);			//输出bcde
   var str2 = str.slice(2);
   document.write(str2);			//输出cdefg
   var str3 = str.slice(-1);
   document.write(str3);			//输出g
   var str3 = str.slice(-2);
   document.write(str3);			//输出fg
   ```

6. substring(): 截取 （如果是负数则返回整个字符串）

   ```javascript
   var str = 'abcdefg';
   var str1 = str.substring(1,5);
   document.write(str1);			//输出bcde
   var str2 = str.substring(2);
   document.write(str2);			//输出cdefg
   var str3 = str.substring(-1);
   document.write(str3);			//输出abcdefg
   ```

7. trim():  去除前后空格

   ```javascript
   var str = '  abcdefg  ';
   var str1 = str.trim();
   document.write(str1);			//输出abcdefg
   ```

8. toUpperCase(): 将字符串改换成大写

   ```javascript
   var str = 'abc';
   var str1 = str.toUpperCase();
   document.write(str1);			//输出ABC
   ```

9. toLowerCase(): 将字符串转换成小写

   ```javascript
   var str = 'ABC';
   var str1 = str.toLowerCase();
   document.write(str1);			//输出abc
   
   ```

10. split(): 将字符串拆分为数组

    ```javascript
    var str = 'A-B-C';
    var str1 = str.split(‘-’);		//str1==>是数组
    document.write(str1);			//输出A,B,C
    
    ```

11. 例题：去除字符串中的非数字字符

    ```javascript
    var str= 'cvs1r#356g7ad';
    var str1 = str.split('');			// 先把字符串拆成数组
    for(var i=0;i<str.length;i++){
        str1[i] = parseInt(str1[i]);	// 把数组的每个元素强制转换一下，如果不是数
    }									// 字会自动转成NaN
    var str2 = str1.join('');			// 把数组拼接成字符串
    str2 = str2.replace(/NaN/g,'');		// 通过全局搜索把字符串中的所有NaN改成‘’
    document.write(str2);				// 输出字符串中的数字
    
    ```

    