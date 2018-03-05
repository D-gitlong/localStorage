# localStorage
# localStorage用法及加密解密

# 存储字符串、数组
例如：
```
var arr=[1,2,3];
localStorage.setItem("temp",arr); //会返回1,2,3
console.log(typeof localStorage.getItem("temp"));//string
console.log(localStorage.getItem("temp"));//1,2,3
```

# 存储对象
```
var obj = {"a": 1,"b": 2};
obj = JSON.stringify(obj); //转化为JSON字符串
localStorage.setItem("temp2", obj);//返回{"a":1,"b":2}
```

# 获取
```
obj=JSON.parse(localStorage.getItem("temp2"));
```

# 删除
```
localStorage.removeItem("temp2");
```

# 加密
```
encodeURI()
var user = {"a": 1,"b": 2};
如：localStorage.setItem("u", encodeURI(JSON.stringify(user)));
```

# 解码
```
decodeURIComponent()
如：JSON.parse(decodeURIComponent(localStorage.getItem("u")));
```



