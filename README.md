
http://www.plantuml.com 官方网站<br>
http://www.plantuml.com/plantuml/form 在线设计器<br>

# 将plantuml嵌入github文档中<br>

### 在github上提交plantuml文件
github上的设计代码，通过plantuml网站在线解析的方法，实现图片展现<br>
1.添加一个任何后缀的文件，这里以example.puml举例，内容如下：
````xml
  @startuml
  Bob -> Alice : hello
  @enduml
```` 
2.在文件列表中查看文件，选择RAW查看，获得该文件的二进制访问链接<br>
https://raw.githubusercontent.com/maobuji/plantuml-example/master/example.puml


### 方法1：直接引用（只能是png，且可能存在缓存问题，优点是简单）<br>

使用plantuml提供的转换器转换为图片<br>
````xml
http://www.plantuml.com/plantuml/proxy?src=后边是文件链接
````

例如以下链接，返回的就是一个png，可以直接用于网页图片的嵌入<br>
http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/maobuji/plantuml-example/master/example.puml

效果如下：<br>
![example.puml](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/maobuji/plantuml-example/master/example.puml)

### 方法2：间接引用<br>

1.访问在线编辑器,使用!includeurl进行一次转换,链接地址就用之前的uml文件地址
````
@startuml
!includeurl https://raw.githubusercontent.com/maobuji/plantuml-example/master/example.puml
@enduml
````

2.获取PNG或者SVG链接地址
点击“View as PNG“或“View as SVG“按钮获取链接地址。

3.将其当作图片嵌入到github中。

# 下载jar包在本地使用<br>
![jar包下载地址](https://jaist.dl.sourceforge.net/project/plantuml/plantuml.jar)
````
// centos使用前需要安装图形组件，否则会报找不到/usr/bin/dot错误
yum install graphviz

// 生成png
java -jar plantuml.jar /tmp/text.uml

// 生成生成svg
java -jar plantuml.jar /tmp/text.uml -tsvg
````