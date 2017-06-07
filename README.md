# jsNode
原生JS移动DOM节点
js-dom

##原生JS DOM操作

###通过ID选取元素 document.getElementById(id) 在低于IE8版本的浏览器，getElementById对匹配元素的ID不区分大小写

###通过name选取元素 name属性只在少数的html元素有效，包括表单、表单元素、iframe和img元素。 document.getElementsByName(name) 在XML文档不可用，返回一个NodeList对象。在IE中，getElementsByName也返回id属性匹配制定值的元素。（避免ID跟name一样） form获取可以通过var form=document.shipgs;

###通过标签名选取元素 document.getElementsByTagName *选择所有

getElementsByName跟getElementsByTagName返回Nodelist，document.images和document.forms的属性为HTMLCollection对象

###通过CSS类选取元素 getElementsByClassName,适用于IE9及以上浏览器

###通过CSS选择器选取元素 querySelectorAll，接受包含一个CSS选择器的字符串参数，返回一个表示文档中匹配选择器的所有元素的NodeList对象。如果没有匹配元素，将返回一个空的NodeList对象。如果选择器字符非法，将抛出一个异常 querySelector返回第一个匹配的元素（以文档顺序）没有则返回null

###当做节点数的文档

parentNode 该节点的父节点，document则是null
childNodes 只读的类数组对象（NodeList对象）
firstChild、lastChild 该节点的子节点中的第一个和最后一个，没有子节点则为null
nextSibling、previousSibling 该节点的兄弟节点中的前一个和下一个。
nodeType 9代表document节点，1代表element节点，3代表text节点，8代表comment节点（），11代表documentFragment节点
nodeValue text节点或comment节点的文本内容
nodeName 元素的标签名，大写形式
###获取和设置非标准HTML属性

getAttribute获取属性
setAttribute设置属性
hasAttribute检测属性是否存在
removeAttribute删除属性
如果操作包含来自其他命名空间中属性的XML文档，则用getAttributeNS、setAttributeNS、hasAttributeNS、removeAttributeNS
HTML5在element对象上定义了dataset属性，如：dataset.a等于data-a的值
node类型定义了attributes属性，document.body.attributes[0]表示body的第一个属性，document.body.attributes["ONLOAD"]表示onload属性
###创建、插入和删除节点

创建节点createElement，XML中使用createElementNS。另外创建新文档节点的方法是复制已存在节点，cloneNode。除了IE之外document还有一个类似方法叫importNode
插入节点appendChild跟insertBefore
删除和替换节点removeChild、replaceChild
