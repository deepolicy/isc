# isc
http://isc.net.cn/ i 收藏：个人网址收藏，为第三方网站提供收藏接口
# 在线演示
http://t.isc.net.cn/test-isc/
# 接口
## 地址
http://isc.net.cn/api-sc/
## 方式
POST
### JQuery 带 cookie 跨域请求
```
$.ajax("http://isc.net.cn/api-sc/",{
	//提交数据的类型 POST GET
	type:"POST",
	data:{
		query: "check_shoucang",
		href: location.href,

	},
	crossDomain:true,
	datatype: "json",
	xhrFields: {  withCredentials: true  },
	//成功返回之后调用的函数             
	success:function(data,status,xhr){
		console.log("data: ", data)
		var obj = JSON.parse(data)
	}
});	
```
## 功能
### 查询 i 收藏中是否存在该网址

### 添加网址到 i 收藏

### 删除


### 获取 open_id
