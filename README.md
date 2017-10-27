## 目录结构
models: 存放操作数据库的文件
public: 存放静态文件，如样式、图片等
routes: 存放路由文件
views: 存放模板文件
index.js: 程序主文件
package.json: 存储项目名、描述、作者、依赖等等信息

## 依赖包
express: web 框架
express-session: session 中间件
connect-mongo: 将 session 存储于 mongodb，结合 express-session 使用
connect-flash: 页面通知提示的中间件，基于 session 实现
ejs: 模板
express-formidable: 接收表单及文件的上传中间件
config-lite: 读取配置文件
marked: markdown 解析
moment: 时间格式化
mongolass: mongodb 驱动
objectid-to-timestamp: 根据 ObjectId 生成时间戳
sha1: sha1 加密，用于密码加密
winston: 日志
express-winston: 基于 winston 的用于 express 的日志中间件

## 设计
1.注册
  1.1注册页：GET /signup
  1.2注册（包含上传头像）：POST /signup
2.登录
  2.1登录页：GET /signin
  2.2登录：POST /signin
3.登出：GET /signout
4.查看文章
  4.1主页：GET /posts
  4.2个人主页：GET /posts?author=xxx
  4.3查看一篇文章（包含留言）：GET /posts/:postId
5.发表文章
  5.1发表文章页：GET /posts/create
  5.2发表文章：POST /posts
6.修改文章
  6.1修改文章页：GET /posts/:postId/edit
  6.2修改文章：POST /posts/:postId/edit
7.删除文章：GET /posts/:postId/remove
8.留言
  8.1创建留言：POST /posts/:postId/comment
  8.2删除留言：GET /posts/:postId/comment/:commentId/remove
