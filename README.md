# project-archetype
演示`maven archetype`插件的使用
## 使用流程
### 安装archetype
`根目录下`依次执行
```
mvn clean install
mvn clean
mvn archetype:create-from-project
```

跳转到`target/generated-sources/archetype/`
``` 
mvn install
mvn archetype:crawl
```
### 使用archetype

任意目录下
```
mvn archetype:generate  -DinteractiveMode=false  -DarchetypeGroupId=com.github.alonwang  -DarchetypeArtifactId=project-archetype   -DarchetypeVersion=1.0.0-SNAPSHOT  -DartifactId={your artifactId}  -DgroupId={your groupId}  -Dversion=0.0.1-SNAPSHOT -Dxxx=xxx
```

eg.
```
mvn archetype:generate  -DinteractiveMode=false  -DarchetypeGroupId=com.github.alonwang  -DarchetypeArtifactId=project-archetype   -DarchetypeVersion=1.0.0-SNAPSHOT  -DartifactId=alonwang-test  -DgroupId=com.github.alonwang.test -Dserver.ip=123.123.123.123
```