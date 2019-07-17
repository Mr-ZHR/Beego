### 2.3环境搭建

这里默认大家已经搭建好了go语言的开发环境。

- 需要安装Beego源码和Bee开发工具//sudo apt-get install

  ```shell
  $ go get -u -v github.com/astaxie/beego
  $ go get -u -v github.com/beego/bee
  ```

  beego源码大家都了解，就是框架的源码。

  Bee开发工具带有很多Bee命令。比如`bee new`创建项目，`bee run`运行项目等。

  用bee运行项目，项目自带**热更新**（是现在后台程序常用的一种技术，即在服务器运行期间，可以不停服替换静态资源。替换go文件时会自动重新编译。）

  安装完之后，bee可执行文件默认存放在`$GOPATH/bin`里面，所以需要把`$GOPATH/bin`添加到环境变量中才可以进行下一步 

  ```shell
  $ cd ~
  $ vim .bashrc
  //在最后一行插入
  export PATH="$GOPATH/bin:$PATH"
  //然后保存退出
  $ source .bashrc
  ```

  安装好之后，运行`bee new preojectName`来创建一个项目，注意：**通过bee创建的项目代码都是在`$GOPATH/src`目录下面的**

  生成的项目目录结构如下:

  ```shell
  quickstart
  |-- conf
  |   `-- app.conf
  |-- controllers
  |   `-- default.go
  |-- main.go
  |-- models
  |-- routers
  |   `-- router.go
  |-- static
  |   |-- css
  |   |-- img
  |   `-- js
  |-- tests
  |   `-- default_test.go
  |-- views
      `-- index.tpl
  
  ```

  **进入项目目录 **执行`bee run`命令，在浏览器输入网址：127.0.0.1：8080，显示如下： 

  ![1538467908697](.\assets\1538467908697.png)