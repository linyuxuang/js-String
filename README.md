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

解释：该方法是对(数组或者字符串)进行部分截取，
     并返回一个数组副本；
     参数start是截取的开始数组索引，
     end参数等于你要取的最后一个字符的位置值加上1（可选）            
            
            var str="helloworld";
               console.log(str.slice(2))   // lloworld
               console.log(str.slice(1,6))   // ellow
		  	
                     
                     
                     
                     
                     
