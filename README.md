# project-archetype
多模块maven项目生成archetype示范.考虑下面这个场景,新项目需要从老项目移植,有两种做法
1. 将老项目整个复制过去,替换包名,移除冗余业务逻辑代码,修改硬编码...
2. 使用老项目生成archetype,之后再有新项目利用archetype直接生成

如果预期会有很多新项目,2是更优的选择


## 使用流程
1. 安装到本地
切换到target/generated-sources/archetype下执行
```
mvn install
```
2. 生成新项目
无路径要求
```
mvn archetype:generate  -DinteractiveMode=false -DarchetypeGroupId=org.example -DarchetypeArtifactId=project-archetype-archetype -DarchetypeVersion=1.0-SNAPSHOT  -DartifactId=example-project -DgroupId=abc.def.ghk -Dversion=1.0-SNAPSHOT -Dcustom-property=192.168.20.101
```
