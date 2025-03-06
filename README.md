# 🎯 xia_Yue_pro 2.0 

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

![中文编码示例](https://github.com/user-attachments/assets/692f5f08-1610-40fa-a8ee-685006c229c9)

### 2. 请求行参数测试

新增请求行参数替换功能：
- 🆕 支持 URL 参数替换
- 🔄 动态修改请求行参数
- 📝 灵活的参数配置

示例：
输入: token=11111
原始请求: POST /1111.com?token=22222
修改后: POST /1111.com?token=11111

![请求行参数测试](https://github.com/user-attachments/assets/c9b71dc9-3a23-4510-9d83-83e3875e8df8)

## 📝 待办事项

- [ ] 支持更多未授权测试方式
  - [ ] API 路径穿越
  - [ ] JS 文件越权
  - [ ] 更多测试场景...
- [ ] 优化界面交互
- [ ] 添加测试报告导出
- [ ] 完善文档说明

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

[MIT License](LICENSE)

## 🙏 致谢

- [瞎越原版](https://github.com/smxiazi/xia_Yue)
- 所有贡献者

---
⭐️ 如果这个项目对你有帮助，欢迎 Star！
