## Welcome to GitHub Pages-Demo-Liu

**这是一个博客样例,为了方便在 [FreeServer](https://github.com/Demo-Liu/FreeServer) 项目2.0中使用个人博客发布文章, 而又懒癌晚期的小伙伴**

## 如何使用

### 1. Fork 这个仓库,然后进入你Fork仓库的Settings   

  -  修改仓库名称前缀为你的用户名  
     用户名为小写: **{username}**.github.io  
  ![rename](https://github.com/Demo-Liu/MyPicture/raw/master/githubio/rename.png)

### 2. 访问你的个人博客地址查看是否搭建成功
  - 如: [https://demo-liu.github.io](https://demo-liu.github.io)
    出现下图所示,即为成功
    ![pages](https://github.com/Demo-Liu/MyPicture/raw/master/githubio/pages.png)
    
### 3.生成ssh key  
  **1)** 首先需要你本地安装了 **Git**  
  - 打开 **Git 命令行**,输入以下命令  
  ```
  cd ~/.ssh
  ```
  如果提示文件夹不存在 输入命令  
  ```
  mkdir ~/.ssh
  ```
  **2)** 设置github用户名和邮箱
  ```
  git config --global user.name "Demo-Liu"
  ```
  ```
  git config --global user.email "demoliu94@163.com"
  ```
  **3)** 生成 ssh Key
  - 输入以下命令,提示输入时直接回车即可
  ```
  ssh-keygen -m PEM -t rsa -b 4096
  ```
  如下图所示,即为成功  
  ![sshkey](https://github.com/Demo-Liu/MyPicture/raw/master/githubio/sshkey.png)
  - 现在查看.ssh文件夹中应包含以下文件, 其中 **id_rsa** 为私钥, **id_rsa.pub** 为公钥 
  (.ssh文件路径为 当前用户根目录下 如windows下为: C:\Users\ **{username}** \.ssh)
  ![sshfile](https://github.com/Demo-Liu/MyPicture/raw/master/githubio/sshfile.png)
### 4.设置仓库公钥
  - 打开 Fork 仓库的 **Settings** --> **Deploy Keys** --> **Add deploy key**
  ![addkey1](https://github.com/Demo-Liu/MyPicture/raw/master/githubio/addkey1.png)
  - 填写 **Title**(任意值), **Key** 为id_rsa.pub中的公钥,使用记事本打开然后copy填写即可
    另外 要勾选 **Allow write access**
  ![addkey2](https://github.com/Demo-Liu/MyPicture/raw/master/githubio/addkey2.png)

### 5.关于私钥的使用
  **私钥为公钥对应key,需要放至FreeServer项目 resources/key/ 目录下, 至此,可以使用FreeServer项目发布的个人博客便搭建完毕**
