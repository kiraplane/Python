# 爬虫笔记
又下定决心开始学习一下python和爬虫，希望这次可以坚持，共勉~

代码、思路是学习的静觅老师的教程，虽然是python2.7的，但依然很实用，我也因此希望先按照教程走一遍再来进阶python3

原博客地址：http://cuiqingcai.com/990.html

### 学习笔记
1. 用python实现爬虫的基本流程和必要条件tips：
- ① python文件中导入库：urllib和urllib2、re正则库
- ② 设置url地址
- ③ 设置Request中的headers，主要为代理，User-Agent
- ④ 用urlopen方法读取Request，其中包含了url和headers，这一步为爬取工作
- ⑤ 用reponse.read()读取第④步的内容，并存在变量中
- ⑥ 设置正则表达式模块（核心部分），对爬取下来的进入进行匹配，需要用到方法，re.compile()和re.match或re.findall
- ⑦ 输出匹配后的内容（可按照自己的需求设计，本次的为按照教程写的面向对象式设计）
- ⑧ 用try except进行错误提示

2. 在学习过程中遇到的坑tips：
- ① python的缩进，非常严格，同一行代码不能同时用TAB和空格，建议都用TAB，查看方法：选中空白后，四个点是空格，一条横杠是TAB
- ② 对基本语法的不熟悉，导致不理解代码的含义，还需要再一步学习，比如list的增删改查，方法、对象等
- ③ 正则表达式的重要性，正则表达式是核心，需要了解惰性和非惰性匹配，本次用的非惰性匹配非常实用，借鉴下别人的理解进行说明：https://github.com/516310189/PythonSpider/tree/master/QSBK
- ④ cookie的用法（虽然本项目没用）：导入cookie库->创建cookie文件->创建代用cookie的opener->访问登录后的url，将cookie保存到文件中->用保存的cookie访问该站点的其他url
