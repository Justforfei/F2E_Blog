##Hash
			http://  	xxx.com   :80 		  /path 			  ?q=a 						  #hash
			协议		 	主机名 	 	端口号	  资源位置	  	query string		  hash Tag
href						host  		port			pathname 			search  					hash

*tips:%20为空格*
<!-- 获取指定的参数的值 -->
```javascript
function getQueryVariable(variable)
{
       var query = window.location.search.substring(1);
       var vars = query.split("&");
       for (var i=0;i<vars.length;i++) {
               var pair = vars[i].split("=");
               if(pair[0] == variable){return pair[1];}
       }
       return(false);
}
```

```javascript
function getQueryVariable(variable) {
	var query = window.location.search.substring(1)
	var vars = query.split("&");
	for (var i=0;i<vars.length;i++) {
	    var pair = vars[i].split("=")
	    if(pair[0] == variable){
        if(pair[1].indexOf('%20') != -1){
            console.log(pair[1].indexOf('%20'))
            var fullName = pair[1].split('%20')
            console.log(fullName)
            return fullName[0] + ' ' + fullName[1]
        }
        else {
            return pair[1];
        }
    }
	}
return(false)
}
```

```javascript
function QueryString(variable) {
    return location.search.substring(1).split("&")
        .map(function (p) { return p.split("=") })
        .filter(function (p) { return p[0] == variable })
        .map(function (p) { return decodeURIComponent(p[1]) })
        .pop();
}
```

```javascript
function QueryString(variable){
        try{
            q = location.search.substring(1);
            v = q.split("&");
            for( var i = 0; i < v.length; i++ ){
                p = v[i].split("=");
                if( p[0] == variable ){
                    if( p[1].indexOf('%20') != -1 ){
                        return decodeURIComponent(p[1]);
                    }
                    else{
                        return p[1];
                    }
                }
            }
        }
        catch (e){
            console.log(e);
        }
    }
```

[1]:[https://css-tricks.com/snippets/javascript/get-url-variables/]
[2]:[http://stackoverflow.com/questions/901115/how-can-i-get-query-string-values-in-javascript#]
