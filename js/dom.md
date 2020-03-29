## dom(js操作html的api)

#### DOM构造函数树

![](C:\Users\53573\AppData\Roaming\Typora\typora-user-images\image-20200328180006476.png)

#### Node.prototype

##### 属性：

1. ###### 层次结构

- parentNode   父节点
- childNodes    获取所有子节点（文本、元素、注释）
- firstChild  获取当前节点的第一个子节点
- lastChild   获取当前节点的最后一个子节点
- nextSibling   获取当前节点下一个兄弟节点
- previousSibling    获取当前节点上一个兄弟节点
- ownerDocument   获取当前document

2. ###### 节点属性

- nodeName  

​                如果文本节点：#text

​                如果元素节点：元素的名称大写

- nodeType

  ​          Node.ELEMENT_NODE

  ​          Node.DOCUMENT_NODE

  ​          Node.COMMENT_NODE

  ​          Node.TEXT_NODE

- nodeValue

  ​        注释节点

  ​        文本节点

##### 方法：

​         【父节点调用的方法】

- appendChild()       追加孩子节点
- insertBefore(new,reference)   将new节点插入到reference之前
- removeChild(child)   移除指定的子节点元素
- replaceChild(new,old)       使用new节点替换old节点
- cloneNode()        克隆节点
- contain()                 判断某个节点是否当前节点的后代节点
- hasChildNodes()   盘点某个节点是否是当前节点的子节点

#### Document.prototype

#####            属性：

- -  head
  - title
  - body
  - forms
  - images
  - hidden
  - links
  - location  跳转

  #####         方法：

  - creatElement(tagName)
  - getElementById()  通过id获取元素
  - getElementByClassName()     通过类名获取元素
  - getElementByTagName()    通过标签名获取元素

#### Element.prototype

#####            属性:

- - children  获取所有子元素
  - firstElementChild  获取当前元素的第一个字元素
  - lastElementChild   获取当前元素的最后一子元素
  - nextElementSibling   获取当前元素的下一个兄弟元素
  - previousElementSibling   获取当前元素的上一个兄弟元素
  - innerHTML   获取或设置元素内部的html,标签可以被解析
  - id
  - className
  - name
  - src
  - href
  - alt
  - clientWidth     宽（padding + 内容）
  - clentHeight     高（padding + 内容）
  - clentTop    上边框的宽度
  - clientLeft     左边框的宽度

  ##### 方法：

  - getAttribute(key)
  - setAttribute(key)
  - querySelect()
  - querySelectAll()

#### HTMLElement

- innerText  设置或获取元素内部的文本内容，标签不会被解析

​       