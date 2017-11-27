docker-php_cli
=============== 

基于Docker官方镜像php:7.1.11-cli制作，集成了pcntl、posix、event等扩展。

## 镜像附加alias命令备忘

### 添加alias命令
编辑bashrc文件
~~~
vi ~/.bashrc
~~~
在尾部添加下面内容
~~~
alias cd-lnmp='cd /mnt/host_d/Docker/compose/lnmp'
alias cd-phpc='cd /mnt/host_d/Docker/compose/php_cli'
alias run-phpc='cd-phpc && docker-compose run --rm -p 8000:8000 php-7.1-cli'
~~~

### 使添加的alias命令立即生效
~~~
source ~/.bashrc
~~~

### 启动php-7.1-cli服务并进入'php -a'交互模式
~~~
run-phpc
~~~

### 启动php-7.1-cli服务并进入bash
~~~
run-phpc bash
~~~

### 启动php-7.1-cli服务并运行shell命令，例如输出'hello world'
~~~
run-phpc echo 'hello world'
~~~