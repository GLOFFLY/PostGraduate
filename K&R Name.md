## 内部变量使用k&r，接口使用驼峰命名法
k&r风格: 讲究简短清爽.单词一致使用小写;一个单词超过8个字符的使用缩写;一个名字中包含多个单词则用下划线隔开它们.
```c
BOOL empty;
int num_element;
void get_element();
class stack;
class seq_stack;
struct student;
object obj;
dialog dlg;
int object::cls_id;
int tmp;
int i, j;
```
## 命名的艺术
一般性原则：
1. 普遍 
* 使用正确的英文术语及其简写
node,child,sibling,parent,root,
first,last,next,previous,
* 避免使用万金油名称：
item、data
* 正确使用时态：
linked list
* 正确使用单数、复数形式：
nodes,children
* 使用喜闻乐见的缩写
nr,sz,dbl,tri,len,max,min,buf,ver,id,
prev,tmp,param,arg,argc,argv,
conn,ctxt,err.
2. 局部变量
尽量简洁：
* 循环：i,j,k;数量：n;长度：len;
* 尺寸：sz;指针：p
* 临时变量：tmp;临时缓冲区：buf;
3. 函数及全局变量的名称
* 接口：
`<type><lib prefix>_<short phrase>(...)`
* 文件内：
`static <type><short phrase>(...)`
* 模块间：
`<type>_<module_prefix>_<short phrase>（）`
GCC可以加上这一句`attribute __((visibility("hidden")))`避免命名污染