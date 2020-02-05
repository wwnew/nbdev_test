
# Title
> summary


# nbdev report���ñ���
nbdev GitHub ��ַ��https://github.com/fastai/nbdev/
nbdev �ĵ���https://nbdev.fast.ai/
> install ��װ���  
> export  �Զ��������� Python ģ��   
> ִ�д��뵼���ͱ༭���������и����Զ������� notebook ��  
> doc �Զ������ĵ�  
> test ����  
> CI ��������  
> version control �汾���ƺͳ�ͻ����  

This file will become your README and also the index of your documentation.

##  Install ��װ���
ʹ��pip����

`pip install nbdev_test`

��װ����github��cloneһ��ģ��https://github.com/fastai/nbdev_template/generate  
Ȼ������е�setup.ini�ļ����б༭

## ����ģ��
### *ʹ�������з�ʽ
ֱ���������д�������nbdev_build_lib ������ͬ��Ŀ¼�����ɶ�Ӧ��.py�ļ�
### *��notebook������cell��ʹ�����е�export����notebook2script 
```python
#hide
from nbdev.export import *
notebook2script()
```
Ȼ�����ǾͿ�����nbdev_testĿ¼�¿����Զ����ɵ��ļ���ͬʱ���ǿ��Դ��е����Ӧ��ģ��ʹ�����ж���ĺ���


```python
from nbdev_test.computer import *
```

## doc �Զ������ĵ�
ʹ�������й���nbdev_build_docs���Զ�����docs������index.ipynb�е����ݸ��µ���Ӧ��readme�ļ��С�  
``` python
#export
def say_hello(to):
    "Say hello to somebody" #������Ϊfunction���������Զ����ĵ�������
    return f'Hello {to}!'
    
assert say_hello("Jeremy")=="Hello Jeremy!"
```
����ʹ�������й��ߣ���������notebook���������´���show_doc(),����celloutput�в鿴�ĵ���������
``` python
from nbdev.showdoc import *
show_doc(HelloSayer.say)
```

## �������Զ����� notebook ��
����������nbdev_update_lib ���lib�еĸĶ����رʼǱ���  
ͨ���޸�lib�ļ�����computer.py��,���Խ�py�ļ��еĸĶ�ͬ����notebook�С���


## ��ʽ��ʾ
���ӣ����Խ���ʽ��ʾ����
```
This version is diplayed inline: $\sum_{i=1}^{k+1}i$ . You can include text before and after.
```
This version is diplayed inline: $\sum_{i=1}^{k+1}i$ . You can include text before and after.
