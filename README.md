# kibana 在线实验环境

## 软件简介

Kibana是Elasticsearch的开源数据可视化插件。它在Elasticsearch集群上索引的内容之上提供可视化功能。用户可以在大量数据之上创建条形图，线条和散点图，或饼图和贴图

所属类别是企业应用

特点：

安装简易，容易上手

## 软件官网

https://en.wikipedia.org/wiki/Kibana

## Dockerfile 使用方法

### 如何使用
您可以kibana简单地运行默认命令：
```
$ docker run --link some-elasticsearch:elasticsearch -d kibana
```
您还可以传递额外的标志kibana：
```
$ docker run --link some-elasticsearch:elasticsearch -d kibana --plugins /somewhere/else
```
此图像包括EXPOSE 5601（默认port）。如果您希望能够从主机访问没有容器IP的实例，则可以使用标准端口映射：
```
$ docker run --name some-kibana --link some-elasticsearch:elasticsearch -p 5601:5601 -d kibana
```
您还可以通过ELASTICSEARCH_URL环境变量提供弹性搜索的地址：
```
$ docker run --name some-kibana -e ELASTICSEARCH_URL=http://some-elasticsearch:9200 -p 5601:5601 -d kibana
```
然后，通过浏览器http://localhost:5601或http://host-ip:5601浏览器访问它。

## 资源链接

- https://www.oschina.net/p/kibana
- https://en.wikipedia.org/wiki/Kibana
- https://wenku.baidu.com/view/00656472f705cc1754270944.html
