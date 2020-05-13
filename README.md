目前处于代码初期后期会继续更新，欢迎师傅们加QQ提意见：NTYzMTY0NjE3 (防麦片)

# FofaSpider
本脚本基于python3开发

fofa爬虫，支持高级查询语句批量获取域名和ip,自动爬取直到结果为空

为了防止爬取过程中被ban延长了time.sleep()的时间，平均sleep 5秒左右

## 更新日志：
05.13 新增输出结果到文本功能,取消了fakeUseragent的使用

## 目前功能
支持批量爬取功能，将语句写在txt中会进行批量查询(为了防止被ban，爬取周期有可能较长)

支持输出爬取结果到txt文本

### 依赖安装

pip install -r requirements.txt

### 使用方法

**ps：普通用户高级语法查询只支持第一页，非高级语法搜索支持前5页**

## Linux下使用

`python3 Spider.py '你的fofaCookie' -q 'domain="baidu.com"||title="百度"' `

## Windows下使用

windows下使用不需要加引号，windows下的查询语句最好用 \ 转义一下（后面会想办法改）

同时windows的高级语法中的|| && 只能在 -r 读取txt文本的模式下使用

`python3 Spider.py 你的fofaCookie  -q domain=\"baidu.com\" `

## 支持批量查询语句
将查询语句写在txt文档中，一个语句换一行，格式如下:
domain="baidu.com"

domain="bilibili.com"

**Linux下**
`python3 Spider.py -r 你文本的路径 'cookie'`

**Windows下**
`python3 Spider.py -r 你文本的路径 cookie`
