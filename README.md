Spring Data Elasticsearch With Elasticsearch Version 5.5.0 (SDES-550)
=========================

由于早期版本的Spring Data Elasticsearch (SDES)中的Elasticsearch (ES)版本较低，基于Spring Data Elasticsearch
        2.1.9.RELEASE版本，将原来ES的2.4.0版本更改为5.5.0，原SDES的代码请在Github上查看：[Github](https://github.com/spring-projects/spring-data-elasticsearch/tree/2.1.9.RELEASE)
        
帮助
------------

* [Spring Data Elasticsearch参考文档](http://docs.spring.io/spring-data/elasticsearch/docs/current/reference/html/)
* [API Documentation](http://docs.spring.io/spring-data/elasticsearch/docs/current/api/)


说明
-----------
Wiki page for [Getting Started](https://github.com/spring-projects/spring-data-elasticsearch/wiki/How-to-start-with-spring-data-elasticsearch)

### Gradle使用

当项目依赖Spring Boot及使用Dependency Management插件的时候，可能由于收到项目依赖的管理，使得单纯使用该项目依赖时，会出现`elasticsearch`版本号仍然为旧版本，所以可能需要以下的配置。以上未完全验证，只是在实践过程遇到问题时作为一个猜测

```gradle
compile("com.vortex.platform:spring-data-elasticsearch-es550:2.1.9-SNAPSHOT") {
        exclude group: 'org.elasticsearch'
    }

compile group: 'org.elasticsearch', name: 'elasticsearch', version: '5.5.0'
```
