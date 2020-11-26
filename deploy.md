#bridge部署
```javascript
```
##1,静态文件地址在相对路径
```javascript
src/app/static
```

##2,环境变量
```javascript
	MAIN_HOST     = 后端api的访问地址
	REDIS_HOST    = redis的host
	REDIS_PORT    = redis端口
	SQL_NAME      = 数据库用户名 比如 "root"
	SQL_PASSWORD  = 数据库密码 比如 "7811175yy"
	SQL_HOST      = 数据库地址 比如 "127.0.0.1:3306"
	SQL_DATABASE  = SQL DATABASE 比如 "bridge"
	STATIC_FOLDER = 静态文件夹地址，后端地址在 os.path.join(basedir,"app","static") 当中。
	STATIC_HOST   = "http://frp.sealan.tech:20303"

```
#nginx 改写地址
>/api/v1/bridge
改成
>/api/v1/bridge(或者想要给前端的使用的其他地址)
#部署后验证部署成功的测试地址


>/api/v3/bridge/test



#其他手动设置
