---
description: 数据库相关
---

# mongodb

#### Mongodb术语解释

1. **database--database：数据库**
2. **table – collection：数据库表 – 集合**
3. **row – document： 数据记录 – 文档**
4. **column – field：数据字段 – 域**
5. **index – index ：索引 – 索引**
6. **table-join – None：表连接~**
7. **primary key – primary key ：主键**

## 安装Mongodb

* 默认安装完的的文件存放在 /usr/local/Cellar/mongodb 下

{% tabs %}
{% tab title="安装" %}
> brew install mongodb
{% endtab %}

{% tab title="启动服务" %}
> brew services start mongodb
{% endtab %}

{% tab title="停止服务" %}
> brew services stop mongodb
{% endtab %}

{% tab title="进入命令" %}
> mongo
{% endtab %}

{% tab title="查看服务状态" %}
> brew services list
{% endtab %}

{% tab title="启动mongodb" %}
> 打开终端命令，进入mongodb下的bin目录，使用命令 ./mongod 来启动 mongodb服务
{% endtab %}
{% endtabs %}

## 配置Mongodb

* 新建2个目录，第一个是 data/db, 用于存放数据文件；第二个是 etc，用于存放mongodb.conf。
* 在mongodb根目录下创建 data/db 数据文件

> /usr/local/Cellar/mongodb/data/db

* 创建 mongodb.conf

```text
// /usr/local/Cellar/mongodb/etc

#mongodb config file
dbpath=/Users/wangxi/Documents/mongodb/data/db/
logpath=/Users/wangxi/Documents/mongodb/mongod.log
logappend = true
port = 27017
fork = true
auth = true

```

* 把 **/usr/local/Cellar/mongodb/3.6.4/bin** 目录添加到PATH中

> echo 'export PATH=/usr/local/Cellar/mongodb/3.6.4/bin:$PATH'&gt;&gt;~/.bash\_profile

