# 奶茶点餐小程序部署
小组成员：林越
## 1.所需环境
HBuilder X，微信开发者工具，IDEA，Maven，Navicat，Visual Studio Code，Redis
## 2.部署小程序
### （1）
- 将naicha_ui文件夹导入HBuilder X
- 找到manifest.json文件，选择微信小程序配置，将微信小程序AppID换成自己的。
- 找到project.config.json文件，将appid改为自己的。
- 将文件运行到微信开发者工具
### （2）
- 在微信开发者工具中点击详情，将本地设置中不校验合法域名及HTTPS证书勾选上
- 确保安全设置中的服务端口开启
## 3.部署后端
### （1）
- 将naicha文件夹的导入IDEA，ps：jdk 1.8
- 在IDEA设置中找到Maven，配置Maven
- 找到naicha_app/src/main/resources中的application-dev.yml文件，配置图片路径（naicha-img所在路径）复制即可，同时更改数据库密码为自己的。
- naicha_system/src/main/resources中的application-dev.yml进行一样的配置
- 在Navicat中新建数据库，将naicha/sql/naicha.sql导入
- 将naicha_app和naicha_system启动
### （2）
- 此时在微信开发者工具中已经可以进行微信授权登录
## 4. 部署后台管理
### （1）
- 将naicha-admin-ui文件夹导入Visual Studio Code
- 注意node.js的版本,必须使用v12.22.12该版本，可在cmd窗口中输入node -v查看当前版本，如果不匹配，请修改版本
- 在vs code终端中输入npm run dev,运行成功将会出现链接
- 安装redis
- 部署成功
### （2）
- 后台管理员测试用例：用户名：admin  密码：123456