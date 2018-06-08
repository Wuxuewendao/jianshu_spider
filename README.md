# jianshu_spider
爬取简x专题、作者和文章摘要数据的爬虫

### 采集说明
主要收集的数据如下

专题：ID、名称、文章数、粉丝数

作者：ID、昵称、文字总数、粉丝数、喜欢数、

文章：ID、标题、文字数、阅读数、喜欢数、评论数、赞赏数、售价、购买量及发布时间

### 运行环境
`Python 3.6.5`

### 运行方式
1. 新建名为 `jianshu` 的数据库，执行 `jianshu.sql` 简历数据库表结构
2. 运行 `GetCategories.py`，获取所有专题数据
3. 运行 `GetArticles.py`，轮循已获取的专题数据，分别抓取对应专题下所有的文章数据

### Issue
1. 未加入多线程和协程等技术，导致目前采集效率非常低下。由于机制的原因，`GetArticles.py` 在采集过程中需要根据请求结果判断是否存在下一页数据，进而判断是否发起下一次请求

