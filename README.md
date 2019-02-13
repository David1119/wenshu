# 中国裁判文书网爬虫思路分享

仅供学习交流，请勿用于非法途径。

web端加密混淆，并且速度很慢，经常404，遂放弃，从app端入手

app端分析：
 - Fiddler抓包获取接口数据
 - app接口返回数据全部加密
 - app逆向分析发现数据使用AES加密：接口带签名请求数据，从服务器获取加密数据，app生成解密key，解密数据前端展示
 - app中.so文件生成关键数据，根据此值选择20个加密算法中的一个，生成AES key解密接口数据
 - api限流，需代理
 
 基本思路如上，花些时间基本可以搞定，数据如下。有偿提供技术支持 qq：MzgwNzI4NjE4
 
 ![](http://ww1.sinaimg.cn/large/d1cedde3ly1g04iyf4jgyj20wu0bd77v.jpg)
 
