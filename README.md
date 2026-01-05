# 🎯 xia_Yue_pro 

>  瞎越修改版，专注于越权漏洞检测的 Burp Suite 插件

[![GitHub stars](https://img.shields.io/github/stars/h00klod0er/xia_yue_pro)](https://github.com/h00klod0er/xia_yue_pro/stargazers)

基于原版[瞎越](https://github.com/smxiazi/xia_Yue)插件优化，增强越权和未授权测试功能。

# xia Yue Pro v3.0 版本更新日志
1.重构界面，把越权设置和越权结果拆分。

2.添加参数置空越权测试，打开后会自动将POST请求包和json请求包里的数据置空重新发送一遍请求包进行越权测试

3.添加其他常见越权测试方法，可打开其他越权测试进行测试，例如：;.js,/;/等导致的越权
<img width="70%" alt="image" src="https://github.com/user-attachments/assets/5f3414d8-00ab-4165-bcea-e195bad92450" />

<img width="80%" alt="image" src="https://github.com/user-attachments/assets/c41ca474-486b-4f43-93ac-7d73bdc05fc5" />

4.添加多身份越权测试功能，开启后可以填入多个不同权限的cookie等字段进行越权测试
<img width="80%" alt="image" alt="image" src="https://github.com/user-attachments/assets/a2a85783-e9eb-4d27-9505-ef27888be580" />



# xia Yue Pro V2.5 版本更新日志

## 新增功能
1. 后缀黑名单功能
   - 可以配置不需要进行越权测试的文件后缀
   - 默认跳过 html 静态页面，也可以添加其他静态页面跳过
   - 支持多个后缀名配置，用逗号分隔
   - 可以随时启用/禁用
   <img width="40%" alt="image" src="https://github.com/user-attachments/assets/023850e3-c93e-497a-9a66-b1fd5d299181" />

2. 手动测试模式
   - 新增"仅接受右键发送的包进行越权测试"选项
   - 打开后仅接受右键中“send to xiayue”的请求包进行越权测试，不会自动进行越权测试
   <img width="40%" src="https://github.com/user-attachments/assets/dc4426f2-5bfe-4eb9-a384-73bae57e3811" />

3. 仅显示越权请求
   - 新增复选框，可以只显示存在越权的请求，方便快速查看越权请求包
   <img width="30%" alt="image" src="https://github.com/user-attachments/assets/58e03578-7e54-462d-acb6-f62cd12fe4f9" />

4.添加jdk8编译的版本，大家自测

## 功能优化
1. 添加请求体越权测试
   - 支持替换请求行和 POST 请求体中的认证参数
   - 可以处理 application/x-www-form-urlencoded 类型的请求体
  

## ✨ 特性

- 🛠️ 修复中文重放乱码问题
- 🔍 支持请求行参数越权测试
- 🚀 添加对比视图，可对比请求和响应（方便截图）
- 💡 可一键复制存在越权的URL，一键发送请求包中的cookie到插件
- 🔄 添加允许重复URL请求越权测试功能，适用于多个功能只通过一个URL进行请求的系统

## 🔨 功能改进

### 1. 中文编码优化 

修复了原版插件在重放请求时中文出现乱码的问题：
- ✅ 修复中文乱码问题，设置UTF-8 编码即可正常使用
- ✅ Burp Suite 2024.3 测试没有问题，可自行测试

<img src="https://github.com/user-attachments/assets/692f5f08-1610-40fa-a8ee-685006c229c9" width="50%">

### 2. 请求行参数测试

新增请求行参数替换功能：
- 🆕 支持 URL 参数替换

示例：输入: token=11111
原始请求: POST /1111.com?token=22222
修改后: POST /1111.com?token=11111


<img src="https://github.com/user-attachments/assets/c9b71dc9-3a23-4510-9d83-83e3875e8df8" width="50%">

### 3. 可一键发送cookie和请求包到插件分析
右键菜单
set cookie 可直接设置插件中越权cookie
sed to xiayue 可发送请求包到插件进行测试

<img src="https://github.com/user-attachments/assets/008668e8-82b1-4903-8b88-2508a9e35848" width="50%">

### 4. 添加对比视图功能，可直观看到原始和低权限响应包对比（方便截图）

点击请求包即可看到

<img src="https://github.com/user-attachments/assets/36dec689-ed2a-4c2b-b2a8-29c8faa708c8" width="50%">

### 5. 添加允许重复请求功能，对于某些系统可能存在URL一致，body不同的情况测试越权

原版插件会对url进行限制，相同的URL只会请求一次，当遇到系统使用同一个接口传参，存在URL一致，body不同的情况可以开启此功能

<img src="https://github.com/user-attachments/assets/ef62d3ea-dcc0-4ff5-8611-5dd14c961774" width="50%">

### 6. 添加一键复制所有越权URL的功能

点击后可直接复制存在越权和未授权的url

<img src="https://github.com/user-attachments/assets/7a9adeca-b831-4514-bee0-9621129c5407" width="50%">
<img src="https://github.com/user-attachments/assets/73f8e862-b11b-424a-9c52-ac5b56ca252d" width="50%">

复制后的效果如下

<img src="https://github.com/user-attachments/assets/6aa2a441-27ed-45b2-903c-f35ac8b211e4" width="50%">

## 📝 待办事项

- [ ] 支持更多未授权测试方式
  - [ ] API 路径穿越
  - [ ] JS 文件越权
  - [ ] 更多测试场景...
- [ ] 优化界面交互

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！


## 🙏 致谢

- [瞎越原版](https://github.com/smxiazi/xia_Yue)
- 所有贡献者

## ⚠️ 免责声明

本工具仅用于授权的企业安全建设：
- 使用本工具时需确保符合当地法律法规
- 使用本工具造成的任何非法后果由使用者承担
- 使用本工具即视为同意本免责声明

本工具仅能在取得足够合法授权的企业安全建设中使用，在使用本工具过程中，您应确保自己所有行为符合当地的法律法规。
如您在使用本工具的过程中存在任何非法行为，您将自行承担所有后果，本工具所有开发者和所有贡献者不承担任何法律及连带责任。

除非您已充分阅读、完全理解并接受本协议所有条款，否则，请您不要安装并使用本工具。
您的使用行为或者您以其他任何明示或者默示方式表示接受本协议的，即视为您已阅读并同意本协议的约束。

---
⭐️ 如果这个项目对你有帮助，欢迎 Star！
