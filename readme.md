### Sonar会用到ElasticSearch，但是ElasticSearch 不支持root账号执行，所以需要用其他账号运行。

#### 步骤如下：

1：准备账号，无论是新建还是用旧的账号，必须给予sonar的目录权限。


2：设置sonar.properties
sonar.search.javaAdditionalOpts=-Dbootstrap.system_call_filter=false

3： 设置wrapper.conf
wrapper.java.additional.1=-Dsonar.wrapped=true
-Dbootstrap.system_call_filter=false

4： 添加内容：/sonarqube-7.8/elasticsearch/config/elasticsearch.yml
bootstrap.memory_lock: false
bootstrap.system_call_filter: false
