# docker-php_cli

php-7.1.11-cli

安装了pcntl、posix、event等扩展

# 备忘

添加alias命令:
1、vi ~/.bashrc（在尾部添加下面内容）          
      alias cd-lnmp='cd /mnt/host_d/Docker/compose/lnmp'
      alias cd-phpc='cd /mnt/host_d/Docker/compose/php_cli'
      alias run-phpc='cd-phpc && docker-compose run --rm -p 8000:8000 php-7.1-cli'
2、source ~/.bashrc（使添加的alias命令立即生效）
3、run-phpc bash（启动php-7.1-cli服务并进入bash） 
4、run-phpc echo 'hello world'（启动php-7.1-cli服务输出'hello world'）
 