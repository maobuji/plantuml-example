
http://www.plantuml.com 官方网站

http://www.plantuml.com/plantuml/from 在线设计器


github上的设计代码，通过plantuml网站在线解析的方法
1.添加一个任何后缀的文件，这里以example.puml举例，内容如下：
````xml
  @startuml
  Bob -> Alice : hello
  @enduml
```` 
2.在文件列表中查看文件，选择RAW查看，获得该文件的二进制访问链接
https://raw.githubusercontent.com/maobuji/plantuml-example/master/example.puml


3.使用
````xml
http://www.plantuml.com/plantuml/proxy?src=后边是文件链接
````

例如：
http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/maobuji/plantuml-example/master/example.puml

效果如下：
![example.puml](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/maobuji/plantuml-example/master/example.puml)


