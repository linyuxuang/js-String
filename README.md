# js-String
js-常用的字符串操作



charAt(参数)  里面的参数代表某个字符串所指定的小标    获取指定下标的字符串值


                var string="12345";
                     console.log(string.charAt(2))   //3

      这样和上面charAt()方式一样
      
                var string="12345";
                     console.log(string[1])   //2
                     
                     
                     
 concat() 合并多个字符串  

                 var srting="12345";
                     console.log(srting.concat("u","w"))   //12345uw
                     console.log(string[1])   //12345 
                     
                     
                     
slice()用法：array.slice(start,end)

解释：该方法是对(数组或者字符串)进行部分截取，并返回一个数组副本；
参数：start是截取的开始数组索引，
     end参数等于你要取的最后一个字符的位置值加上1（可选）            
            
            var str="helloworld";
               console.log(str.slice(2))   // lloworld
               console.log(str.slice(1,6))   // ellow
		  	
                     
                    
substr()  用法：stringObj.substr(start [, length ])

解释：在字符串中抽取从start位置开始的指定长度的子字符串。

参数：start：必选项。所需的子字符串的起始位置。字符串中的第一个字符的索引为 0。
     length：可选项。指定的返回子字符串长度，当省略该值时，表示抽取从start位置到stringObj末尾的子字符串。当该值为0或负数时，将返回一个空字符串                    

          var str="helloworld";
           console.log(str.substr(2,3))   // llo	    
           
	   

substring() 用法：stringObj.substring(start, end)

解释：截取字符串指定范围内的子字符串，含头不含尾即[start,end)。

参数：start：指明截取的起始位置，该索引从 0 开始起算。
     end：指明截取的结束位置，"注意(该索引从 0 开始起算)"。当省略该值时，则截取从开始位置到stringObj末尾的字符串。
     

说明:

1.subtring方法使用start和end两者中的绝对值作为子字符串的起始点。例如，str.substring(0,3)和str.substring(0,3)的结果是一样的。

2.如果start或end为NaN或者负数，那么该参数将会被自动替换为0。

3.截取的字符串长度是start-end的差的绝对值，即：|start-end|=length     
	   
	   
	   
		  	var str="helloworld";
		  	 console.log(str.substring(2,3))   // l
	   
	   
	   
 indexOf返回字从（左往右）的字符串第一次出现的位置，若没有出现返回-1  

		 var str = "hello world";
		  console.log(str.indexOf("o"))//显示4
		  console.log(str.indexOf("i"))//显示-1                    


lastIndexOf
lastIndexOf()方法返回（从右向左）出现某个字符或字符串的首个字符索引值（与indexOf相反）

			 var str = "hello world";
			  console.log(str.indexOf("o"))//显示7
			  console.log(str.indexOf("i"))//显示-1  
		

indexOf()与lastIndexOf()有两个参数时     注意看下面


		  	var str="hello world";
		  	 console.log(str.indexOf("o",6))   // 7
		  	 console.log(str.lastIndexOf("o",6))  //4


                     
		  	var strVal="abcdefacdfghajk";
		  	 var pos=new Array();
		  	var strIndexOf=strVal.indexOf("a");
		  	 while(strIndexOf>-1){
		  	 	 pos.push(strIndexOf);
                         strIndexOf=strVal.indexOf("a",strIndexOf+1);
		  	 }
		  	 console.log(pos)     //0  6  12


trim() 删除字符串左右空格          trimLeft()删除左边空格           trimRight()删除右边空格


			var str="    linyuxuan     ";
			
			 var Trim=str.trim();
			 console.log(str);    输出  "    linyuxuan     "
			 console.log(Trim);  输出 "linyuxuan"

toLocaleUpperCase()转大写                toLocaleLowerCase() 转小写


		var str="linyuxuan";
          	console.log(str.toLocaleUpperCase())    // 输出 LINYUXUANPP
          	
          	 var str2="LINYUXUANPP";
          	 console.log(str2.toLocaleLowerCase())   //输出 linyuxuanpp
		 

字符串的匹配模式

match()  返回是一个数组     在字符串该方法，本质上与调用RegExp的exec()方法相同 ，match() 方法接受一个参数

                 var text="cat bat sat hat lopp";
          	  var pat=/.at/g;      这里的代表查找全局at,
          	  var matches=text.match(pat);
		  console.log(matches[1])  输出  cat
          	  console.log(matches[2])  输出 bat

       如果不加 “g”    这里只能查到第一个带 at 的字符
        
	     var text="cat bat sat hat lopp";
          	  var pat=/.at/;  
          	  var matches=text.match(pat);
          	  console.log(matches[0])  输出 bat
                   console.log(matches[1])  输出   undefined 

search() 方法返回字符串中第一个匹配的索引(下标)  如果没有找到 ， 就返回 -1； 该方法始终都是从字符串开头向后查找

         该方法就是添加 “g”全局 他也只会查找第一个
  	  var text="cat bat sat hat lopp";
          	  var pat=/.at/g;
          	  var matches=text.search(pat);
          	  console.log(matches)     输出 0


  	   var text="yu cat bat sat hat lopp";
          	  var pat=/.at/g;
          	  var matches=text.search(pat);
          	  console.log(matches)   输出  3 (就是cat)


replace()   这个方法提供两个参数 
         
	 第一个参数 是一个RegExp或者是一个字符串；
	 第二个参数 是一个字符串，或者是一个函数；
	 (如果第一个参数是一个字符串，那么只会替换第一个字符串，如果要替换所有的字符串，唯一的办法就是一个正则表达式，且要指定全局(g)标志)
	 
	      	  var text="yu cat bat sat hat lopp";
          	  var pat=text.replace('at',"oop");

          	  console.log(pat)    输出  yu coop bat sat hat lopp
		  
		  
		 var text="yu cat bat sat hat lopp";
          	 var pat=text.replace(/at/g,"oop");   
		    console.log(pat)   输出   yu coop boop soop hoop lopp 
		    
		  
		  
	     
	 
	 
	 
	 
	 
	 
	 
	 
	 
	 
	 

