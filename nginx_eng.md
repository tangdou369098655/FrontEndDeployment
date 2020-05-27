@[Host your website with Nginx for Front-end Developers on CentOS](https://github.com/tangdou369098655/FrontEndDeployment/edit/master/nginx_eng.md)

English | [简体中文](https://github.com/tangdou369098655/FrontEndDeployment/blob/master/nginx_zh.md)

## Introduction

* The purpose of this paper is to solve the static resource deployment requirements of the front end by using the simplest and fastest method.
* The company usually uses **tomcat** to deploy a lot of static resources. I bought a server in March this year. I've been busy working overtime and haven't started using it yet. I just used it today.


## Precondition

>ou have a server~~ just like this


![在这里插入图片描述](https://img-blog.csdnimg.cn/2020052418024250.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)

## Step 1: link the server
### 1. Find public IP
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524180429583.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 2. Change Password 
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524180617977.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 3. Download FinalShell, install and open 
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524180724186.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 4. Open FinalShell
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524180916232.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524181021305.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### You can fill in the name at will, you can create a server name which is convenient for later link use.
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524181139763.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 5. Linked server
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524181328551.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200524181539512.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
## Step 2: Install Nginx

 ### 1. Download Nginx package
[Click here to download Nginx compression package](http://nginx.org/en/download.html)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525234600347.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525234634835.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 2. Find the path and drag in the compressed package you just downloaded.
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235141146.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020052523522440.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235306337.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235349136.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235420732.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 3. Decompression files, Refresh directories


```bash
 tar -zxvf nginx-1.18.0.tar.gz
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235716891.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200525235914473.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 4. Installation dependency
 

```bash
yum -y install gcc zlib zlib-devel pcre-devel openssl openssl-devel
```


![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526000500659.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 5. Enter directory, execute command
 

```bash
cd nginx-1.18.0
 
./configure
 
make install
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526001053428.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526001329176.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526001644154.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 6.Configure
To configure this item, you can operate according to the demand or not, and use the default port number

```bash
# Open configuration file
vi /usr/local/nginx/conf/nginx.conf
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526002812672.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526002904509.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
Open the configuration file, use the down arrow of the keyboard to search for the port number and modify it.

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526003012248.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
> Edit and save files nuder Linux
> 
>1.  Using the CD command to enter the file directory ; 
>such as : cd xxx/xxx
>2.  Use vi command to enter the file to be edited and enter normal mode to view the file content; 
>such as : vi xxx
>3.  Enter lowercase 'i' to enter editing mode and start editing text.
>4.  After editing, press 'ESC' to exit to normal mode.
>5.  In normal mode, you can enter ':' to enter command mode.
>6.  Enter ':wq' or 'wq' in command mode to save and exit.

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526005329704.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
### 7.Start Nginx

```bash
/usr/local/nginx/sbin/nginx -s reload
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526235940134.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)

### 8.Check whether Nginx process is started

```bash
ps -ef | grep nginx

```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200527000049159.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
## Step 3: Test

###  1. Enter the server management interface and configure the security group.
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526012658787.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 2. Visit the website
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526012725657.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526012754826.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
## Step 4: Deploy other projects

 ### 1. Enter the static resource directory of the server, drag the packed project to put.
 >Directory address：/usr/local/nginx/html
 
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526233123762.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
 ### 2. Visit
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200526233612452.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3Rhbmdkb3UzNjkwOTg2NTU=,size_16,color_FFFFFF,t_70)
## 结语
> 本教程旨在快速完成项目部署，其他配置项问题没有列举出来哦...后期有空会增加配置文章哟~~
> 欢迎大家指出文章需要改正之处~  
> 如果有更好的方法，欢迎大家提出来，共同进步哟~~ 
