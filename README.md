
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
### 使用命令行方式
直接在命令行窗口输入nbdev_build_lib
### 在notebook最后插入cell，使用其中的export包，notebook2script

然后我们就可以在nbdev_test目录下看到自动生成的文件，同时我们可以从中导入对应的模块使用其中定义的函数


```python
from nbdev_test.computer import *
```


```python
## doc 自动生成文档

```
