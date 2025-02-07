# xia_Yue_pro 2.0 （xia_Yue 修改版）
瞎越修改版，修复中文重放乱码以及添加请求行越权测试功能

# 说明
瞎越是一款主要用于测试越权、未授权的burp插件，原插件地址：https://github.com/smxiazi/xia_Yue
此插件主要在原插件基础添加部分功能和修复bug。

# 修改事项

## 1.原版插件似乎存在重放时中文乱码的情况，于是进行了修改，BURP版本2024.3 字符设置UTF-8 测试似乎没有问题，可以自行测试
![image](https://github.com/user-attachments/assets/692f5f08-1610-40fa-a8ee-685006c229c9)

## 2.在测试中遇到了一个场景，请求行携带token的情况，于是添加了请求行替换和修改功能，勾选此选项，然后在下列输入框输入，即可替换请求行
例如输入 token=11111 ，则会替换请求行中参数POST /1111.com?token=22222 为  POST /1111.com?token=11111
![image](https://github.com/user-attachments/assets/c9b71dc9-3a23-4510-9d83-83e3875e8df8)

# todo
添加其它未授权测试方式，例如api通过;.js越权等
