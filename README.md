docker-php_cli
=============== 

基于Docker官方镜像php:7.1.13-cli-jessie制作，集成了pcntl、posix、event等扩展。

## 镜像附加alias命令备忘

### 添加alias命令
编辑bashrc文件
~~~
vi ~/.bashrc
~~~
在尾部添加下面内容
~~~
alias cd-dc='cd /mnt/host_d/Docker/compose'
alias run-pc='cd-dc && cd php_cli && docker-compose run --rm -p 8000:8000 php71-cli-service'
~~~

### 使添加的alias命令立即生效
~~~
source ~/.bashrc
~~~

### 启动php-cli服务并进入'php -a'交互模式
~~~
run-pc
~~~

### 启动php-cli服务并进入bash
~~~
run-pc bash
~~~

### 启动php-cli服务并运行shell命令，例如输出'hello world'
~~~
run-pc echo 'hello world'
~~~