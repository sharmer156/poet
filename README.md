# poet
我是“小诗姬”，全唐诗作为训练数据。可以写押韵自由诗、藏头诗、给定若干字作为主题的诗。
<br /> <br /> 
环境要求：windows 10和unbuntu都正常运行
---
python:3.x <br /> 
tensorflow  1.x


缺少库 word2vec

使用
```
$conda install word2vec
```
安装
<br /> <br /> 
运行<br /> 
---
运行训练：python train.py <br /> 
---
![image](https://github.com/norybaby/poet/blob/master/doc/train.png)

<br /> <br /> 
 
 
运行写诗服务: 
```
$python poem_server
```
windows
```
python poem_server.py
```
python poem_server<br /> 
---
此步需要先运行训练产生好模型后。

客户端用浏览器访问，效果参照：<br /> 
---
![image](https://github.com/norybaby/poet/blob/master/doc/client.png)

<br /> <br /> 
 ---
```
if poem_style == 1:
        return  writer.free_verse()
    elif poem_style == 2:
        return writer.rhyme_verse()
if  start_with:
         if poem_style == 3:
            return  writer.cangtou(start_with)
         elif poem_style == 4:
            return writer.hide_words(start_with)
 ```           
 ---
 http://127.0.0.1:5000/poem?style=1             # 自由写诗
 
 http://127.0.0.1:5000/poem?style=2             # 押韵写诗
 
 http://127.0.0.1:5000/poem?style=3&start=      # 藏头写诗
 
  http://127.0.0.1:5000/poem?style=4&start=     # 隐字写诗（藏头中的一个字 押韵写诗）
  
如有问题欢迎讨论 xiuyunchen@126.com

