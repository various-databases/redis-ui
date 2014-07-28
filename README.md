phpRedisAdmin
=============

phpRedisAdmin是用于管理[Redis](http://redis.io/)数据库的一个简单界面服务.

安装配置
======================

通过[composer](http://getcomposer.org/)安装，执行如下命令:

```
curl -s http://getcomposer.org/installer | php
php composer.phar create-project -s dev erik-dubbelboer/php-redis-admin path/to/install
```

You may also want to copy include/config.simple.inc.php to include/config.inc.php
and edit it with your specific redis configuration.

或者使用如下方式安装:

```
git clone https://github.com/huge-data/redis-ui.git
cd redis-ui/phpRedisAdmin
git clone https://github.com/nrk/predis.git vendor
```
将phpRedisAdmin放到ngxin下：

```
sudo cp -r phpRedisAdmin /user/share/nginx/html/
sudo chown -R http:http phpRedisAdmin
```

配置config.inc.php:

```
cd phpRedisAdmin/includes
sudo cp config.sample.inc.php config.inc.php
```

具体配置文件参考示例文件config.inc.php.example。


功能
====

* 编码支持编辑
* Javascript实现表排序
* 更好的错误处理机制
* 支持不同服务器之间的key拷贝移动
* 支持JSON格式导入
* 自定义分隔符导出数据
