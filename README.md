![image](https://github.com/user-attachments/assets/e549b132-959d-46a8-b847-e630cc42969d)# 🎯 xia_Yue_pro 2.0 

> 🔄 瞎越修改版，专注于越权漏洞检测的 Burp Suite 插件

[![GitHub stars](https://img.shields.io/github/stars/yourusername/xia_yue_pro)](https://github.com/yourusername/xia_yue_pro/stargazers)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

基于原版[瞎越](https://github.com/smxiazi/xia_Yue)插件优化，增强越权和未授权测试功能。

## ✨ 特性

- 🛠️ 修复中文重放乱码问题
- 🔍 支持请求行参数越权测试
- 🚀 优化性能和用户体验
- 💡 更直观的界面展示

## 🔨 功能改进

### 1. 中文编码优化 

修复了原版插件在重放请求时中文出现乱码的问题：
- ✅ 支持 UTF-8 编码
- ✅ 兼容 Burp Suite 2024.3
- ✅ 完整的中文支持

<img src="https://github.com/user-attachments/assets/692f5f08-1610-40fa-a8ee-685006c229c9" width="50%">


### 2. 请求行参数测试

新增请求行参数替换功能：
- 🆕 支持 URL 参数替换
- 🔄 动态修改请求行参数
- 📝 灵活的参数配置

示例：
输入: token=11111
原始请求: POST /1111.com?token=22222
修改后: POST /1111.com?token=11111

<img src="https://github.com/user-attachments/assets/c9b71dc9-3a23-4510-9d83-83e3875e8df8" width="50%">

### 3.可一键发送cookie和请求包到插件分析
右键菜单
set cookie 可直接设置插件中越权cookie
sed to xiayue 可发送请求包到插件进行测试
![image](https://github.com/user-attachments/assets/008668e8-82b1-4903-8b88-2508a9e35848)

### 4.添加对比视图功能，可直观看到原始和低权限响应包对比（方便截图）

点击请求包即可看到
![image](https://github.com/user-attachments/assets/36dec689-ed2a-4c2b-b2a8-29c8faa708c8)

### 5.添加允许重复请求功能，对于某些系统可能存在URL一致，body不同的情况测试越权

原版插件会对url进行限制，相同的URL只会请求一次，当遇到系统使用同一个接口传参，存在URL一致，body不同的情况可以开启此功能

![image](https://github.com/user-attachments/assets/ef62d3ea-dcc0-4ff5-8611-5dd14c961774)


### 6.添加一键复制所有越权URL的功能

点击后可直接复制存在越权和未授权的url
![image](https://github.com/user-attachments/assets/7a9adeca-b831-4514-bee0-9621129c5407)
![image](https://github.com/user-attachments/assets/73f8e862-b11b-424a-9c52-ac5b56ca252d)
复制后的效果如下
![image](https://github.com/user-attachments/assets/6aa2a441-27ed-45b2-903c-f35ac8b211e4)


## 📝 待办事项

- [ ] 支持更多未授权测试方式
  - [ ] API 路径穿越
  - [ ] JS 文件越权
  - [ ] 更多测试场景...
- [ ] 优化界面交互


## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

[MIT License](LICENSE)

## 🙏 致谢

- [瞎越原版](https://github.com/smxiazi/xia_Yue)
- 所有贡献者

## 免责声明
本工具仅用于授权的企业安全建设
使用本工具时需确保符合当地法律法规
使用本工具造成的任何非法后果由使用者承担
使用本工具即视为同意本免责声明
本工具仅能在取得足够合法授权的企业安全建设中使用，在使用本工具过程中，您应确保自己所有行为符合当地的法律法规。
如您在使用本工具的过程中存在任何非法行为，您将自行承担所有后果，本工具所有开发者和所有贡献者不承担任何法律及连带责任。
除非您已充分阅读、完全理解并接受本协议所有条款，否则，请您不要安装并使用本工具。
您的使用行为或者您以其他任何明示或者默示方式表示接受本协议的，即视为您已阅读并同意本协议的约束。
---
⭐️ 如果这个项目对你有帮助，欢迎 Star！
