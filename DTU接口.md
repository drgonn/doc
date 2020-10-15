##DTU接口
###1、查看单个DTU接口
```javascript
请求方式：GET
请求URL：http://frp.sealan.tech:20303/api/v1/bridge/dtu/<int:id>
测试URL：frp.sealan.tech/api/v1/bridge/dtu/<int:id>
数据格式：JSON
请求说明： 根据DTUID查看单个DTU
```
**返回示例**
> 正常情况下，会返回下述JSON数据包
```javascript
```javascript
{
	'success': true,
	'error_code': 0,
	'records':{
		'name':'名称',
		'sn':'编号',
		'dtu_img':'图片',
		'fault':'是否故障',
		'install_time':'安装时间',
		'update_time':'更新时间',
		'create_time':'创建时间',
	}
}
```
###2、创建DTU接口
```javascript
请求方式：POST
请求URL：http://frp.sealan.tech:20303/api/v1/bridge/dtu
测试URL：frp.sealan.tech/api/v1/bridge/dtu
数据格式：JSON
请求说明： 创建DTU
```
*请求参数说明*

| 参数  | 类型   | 是否必须 | 说明        |
| ----- | ------ | -------- | ----------- |
|name|str|是|名称|
|sn|str|是|编号|
|dtu_img|str|否|图片|
|install_time|time|否|安装时间|

**返回示例**
> 正常情况下，会返回下述JSON数据包
```javascript
{
	'success': true,
	'error_code': 0
}
```
###3、修改DTU接口
```javascript
请求方式：PUT
请求URL：http://frp.sealan.tech:20303/api/v1/bridge/dtu/<int:id>测试URL：frp.sealan.tech/api/v1/bridge/dtu/<int:id>
数据格式：JSON
请求说明： 根据DTUID修改DTU
```
*请求参数说明*

| 参数  | 类型   | 是否必须 | 说明        |
| ----- | ------ | -------- | ----------- |
|name|str|否|名称|
|sn|str|否|编号|
|dtu_img|str|否|图片|
|fault|bool|否|是否故障|

**返回示例**
> 正常情况下，会返回下述JSON数据包
```javascript
{
	'success': true,
	'error_code': 0
}
```
###4、删除DTU接口
```javascript
请求方式：DELETE
请求URL：http://frp.sealan.tech:20303/api/v1/bridge/dtu
数据格式：JSON
请求说明： 根据DTUID删除DTU
```
*请求参数说明*

| 参数  | 类型   | 是否必须 | 说明        |
| ----- | ------ | -------- | ----------- |
|ids|list|是|要删除的id列表|
**返回示例**
> 正常情况下，会返回下述JSON数据包
```javascript
{
	'success': true,
	'error_code': 0
}
```
###5、获取DTU分页列表接口
```javascript
请求方式：GET
请求URL：http://frp.sealan.tech:20303/api/v1/bridge/dtu/list
测试URL：frp.sealan.tech/api/v1/bridge/dtu/list
```数据格式：JSON
请求说明： 获取DTU分页列表接口
```
*请求参数说明*

| 参数  | 类型   | 是否必须 | 说明        |
| ----- | ------ | -------- | ----------- |
|current|int|否|页位置|
|pageSize|int|否|单页条数|
|sorter|object|否|排序参数，格式例如：{'price':'desend'}，就是按价格降序|

**返回示例**
> 正常情况下，会返回下述JSON数据包
```javascript
{
	'success': true,
	'error_code': 0,
	'total':'总条数',
	'data':[
		{
			'id':'DTUID',
			'name':'名称',
			'sn':'编号',
			'dtu_img':'图片',
			'fault':'是否故障',
			'install_time':'安装时间',
			'update_time':'更新时间',
			'create_time':'创建时间',
		},
		...
	]
	}
}
```
