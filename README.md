
http://www.plantuml.com 官方网站

http://www.plantuml.com/plantuml/from 在线设计器


github上的设计代码，通过plantuml网站在线解析的方法
1.添加一个任何后缀的文件，内容是plantuml，内容如下：
  --mysql
  @startuml
  Bob -> Alice : hello
  @enduml
  
2.在文件列表中查看文件，选择RAW查看，获得该文件的二进制访问链接


3.使用
http://www.plantuml.com/plantuml/proxy?src={url}

例如：
http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/maobuji/JAVATestProject/master/test.puml

效果如下：
