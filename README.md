# isc
http://isc.net.cn/ i 收藏：个人网址收藏，为第三方网站提供收藏接口
- 统一

- 快速部署

- 网站导出

- 用户导出
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
第三方网站接口 - 帮助文档 - i 收藏
http://isc.net.cn/sc/api-isc-help.html

### 查询 i 收藏中是否存在该网址
   
参数名 | 参数值
-|-
query | "check_shoucang" |
href | location.href |
	    
### 添加网址到 i 收藏

### 删除


### 获取 open_id

### 获取用户在 i 收藏中，本网站域名下的所有网址信息

# 引入 api.js
http://isc.net.cn/sc/api.js


基础：
```
<div id="ishoucang">
	<template v-if="state=='未查询'">
		查询
	</template>
	<template v-if="state=='未登录'">
		登录并收藏
	</template>
	<template v-if="state=='未收藏'">
		添加收藏
	</template>
	<template v-if="state=='已收藏'">
		取消收藏
	</template>
</div>
```
