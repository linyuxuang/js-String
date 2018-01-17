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
	   
	   
                     
