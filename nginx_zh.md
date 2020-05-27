@[超简单的前端静态资源服务器部署--nginx](https://github.com/tangdou369098655/FrontEndDeployment/blob/master/nginx_zh.md)

简体中文 | [English](https://github.com/tangdou369098655/FrontEndDeployment/blob/master/nginx_eng.md)

## 说明

* 本文旨在使用最简单快速的办法，解决前端静态资源部署需求。
* 公司平时使用 **tomcat** 部署静态资源比较多，今年三月份我买了一个服务器，一直忙着加班还没开始用，今天刚好拿来用一下咯：


## 前提
>你要有一个服务器哟~~
>购买后打开就像这个下面这个样子


![在这里插入图片描述](https://img-blog.csdnimg.cn/2020052418024250.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)

## 步骤一：链接服务器
### 1. 找到公网IP
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524180429583.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 2. 修改密码
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524180617977.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 3. 下载FinalShell，安装打开
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524180724186.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 4. 打开FinalShell
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524180916232.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524181021305.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 名称可以随意填写哦~~ 自己起个服务器的名字，方便以后链接使用。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524181139763.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 5. 双击打开，链接成功
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524181328551.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524181539512.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
## 步骤二：安装Nginx

 ### 1. 下载nginx压缩包；
[点我下载nginx](http://nginx.org/en/download.html)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525234600347.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525234634835.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 2. 找到需要安装的路径，把刚刚下载的压缩包拖进去；
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235141146.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020052523522440.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235306337.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235349136.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235420732.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 3. 解压文件，刷新目录


```bash
 tar -zxvf nginx-1.18.0.tar.gz
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235716891.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235914473.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 4. 安装依赖
 

```bash
yum -y install gcc zlib zlib-devel pcre-devel openssl openssl-devel
```


![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526000500659.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 5. 进入目录，执行命令
 

```bash
cd nginx-1.18.0
 
./configure
 
make install
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526001053428.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526001329176.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526001644154.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 6.配置nginx.conf
### 此项可以根据需求进行操作，也可以不配置，使用默认端口号.

```bash
# 打开配置文件
vi /usr/local/nginx/conf/nginx.conf
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526002812672.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526002904509.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 按住下箭头，往下寻找端口号，修改端口号

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526003012248.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
> Linux下编辑文件并保存
> 
>1.  cd到该文件的目录下
>2.  vi  要编辑的文件名，进入普通模式，可查看文件内容
>3.  输入 i  进入编辑模式，开始编辑文本
>4.  编辑之后，按ESC退出到普通模式。
>5.  在普通模式下，输入 : 进入命令模式
>6.  在命令模式下输入wq, 即可保存并退出

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526005329704.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 7.启动nginx

```bash
/usr/local/nginx/sbin/nginx -s reload
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526235940134.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)

### 8.查看nginx进程是否启动

```bash
ps -ef | grep nginx

```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200527000049159.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
## 步骤三：测试

 ### 1. 进入服务器管理界面，配置安全组；
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526012658787.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 2. 测试界面访问
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526012725657.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526012754826.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
## 步骤四：部署其他项目

 ### 1. 进入服务器静态资源目录，拖动打包好的项目放入；
 >目录地址：/usr/local/nginx/html
 
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526233123762.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 2. 访问
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526233612452.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
## 结语
> 本教程旨在快速完成项目部署，其他配置项问题没有列举出来哦...后期有空会增加配置文章哟~~
> 欢迎大家指出文章需要改正之处~  
> 如果有更好的方法，欢迎大家提出来，共同进步哟~~ 
