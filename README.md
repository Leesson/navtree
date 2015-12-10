# navtree
###1.简介
这是一个基于jQuery的导航树插件，适用于多层级数据筛选，和普通的树结构插件类似。不同点在于选中项只有一项，并且选中时只显示与选中项相关的父项和子项，避免数据列表太长时占用页面较大空间
###2.使用方法
和一般jQuery插件一样，此插件使用也很简单便捷。方法是navtree，例如$("#tree").navtree(arr);
####参数
#####dataList    
{Array}|{Object}，传入的参数是数据列表，其中每一项至少包含三个属性，分别是    
- {String}，[identify_field]，数据项的唯一标识字段    
- {String}，[display_field]，数据项要显示的字段，可以和上边同一个字段    
- {Array}，[childs]，数据项的子项列表字段，如果没有可以不设置   

#####opts<br/>

{Object}，初始化参数，包含如下属性，均为可选    
- identify_field，{String}，数据项的唯一标识字段名，默认为"code"    
- display_field，{String}，数据项要显示的字段名，默认"name"    
- selected，{String}，当前选中数据项的唯一标识，默认为""    
- link_to，{String}，筛选树节点的链接，默认"#"    
- title，{String}，筛选树标题名称，默认"navtree"  
- node_style, {String}, 节点显示风格，目前只有两种"default"和"cross"，默认"default"    
- childs_field，{String}，数据项子项列表字段名，默认"childs"    
- callback，{Function}，回调函数，默认无执行效果。含有两个参数，一个是当前选中的树节点对应的数据对象，没有选中项返回null，一个是树的dom    

####代码示例
详见[demo](https://github.com/Leesson/navtree/blob/master/demo.html)    
####效果图    
![tree_0](http://files.cnblogs.com/files/Ghunter/img1.gif)
![tree_1](http://files.cnblogs.com/files/Ghunter/img2.gif)
![tree_2](http://files.cnblogs.com/files/Ghunter/img3.gif)
