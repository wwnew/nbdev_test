
# Title
> summary


# nbdev report试用报告
nbdev GitHub 地址：https://github.com/fastai/nbdev/
nbdev 文档：https://nbdev.fast.ai/
> install 安装软件  
> export  自动创建导出 Python 模块   
> 执行代码导航和编辑，并将所有更改自动导出回 notebook 中  
> doc 自动生成文档  
> test 测试  
> CI 持续集成  
> version control 版本控制和冲突处理  

This file will become your README and also the index of your documentation.

##  Install 安装软件
使用pip命令

`pip install nbdev_test`

安装完后从github上clone一个模板https://github.com/fastai/nbdev_template/generate  
然后对其中的setup.ini文件进行编辑

## 导出模块
### *使用命令行方式
直接在命令行窗口输入nbdev_build_lib 将会在同名目录下生成对应的.py文件
### *在notebook最后插入cell，使用其中的export包，notebook2script 
```python
#hide
from nbdev.export import *
notebook2script()
```
然后我们就可以在nbdev_test目录下看到自动生成的文件，同时我们可以从中导入对应的模块使用其中定义的函数


```python
from nbdev_test.computer import *
```

## doc 自动生成文档
使用命令行工具nbdev_build_docs会自动生成docs，并将index.ipynb中的内容更新到对应的readme文件中。  
``` python
#export
def say_hello(to):
    "Say hello to somebody" #引号内为function描述，会自动在文档中生成
    return f'Hello {to}!'
    
assert say_hello("Jeremy")=="Hello Jeremy!"
```
除了使用命令行工具，还可以在notebook中运行如下代码show_doc(),可在celloutput中查看文档生成内容
``` python
from nbdev.showdoc import *
show_doc(HelloSayer.say)
```

## 将更改自动导回 notebook 中
在命令行中nbdev_update_lib 会把lib中的改动导回笔记本。  
通过修改lib文件（即computer.py）,可以将py文件中的改动同步到notebook中。。


## 公式表示
例子：可以将公式表示出来
```
This version is diplayed inline: $\sum_{i=1}^{k+1}i$ . You can include text before and after.
```
This version is diplayed inline: $\sum_{i=1}^{k+1}i$ . You can include text before and after.
