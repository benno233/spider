spider node 抓取试验
========
试做这个爬虫抓取些妹子图
------------
###2014-9-4
先是试了下 http模块 发送get 请求 获得并输出得到的数据<br/>
然后开始尝试使用node解析html 这部分比较费劲 <br>
先试着用网页源代码中的html结构 然后写相对应的ul、ol等元素 从get到的html数据中 匹配相对应的元素 然后遍历这些元素 从中取得img 最终得到img的src<br>
然后将src用http请求得到图片 再用fs 保存起来(在这之前还要判断下文件路径是否存在，不存在需要创建,用到fs.mkdirSync()或者fs.mkdir(),异步创建效率更高些)<br/>
解析html其实更好的解决方案是使用node-jquery 和前台的jquery使用方法差不多 但是window下安装jquery比较麻烦 主要是jsdom 需要C++ 2010 支持 <br/>
开始安装失败了 后来找到了另一个类似的类库：cheerio 使用和JQ是一样的<br/>
最后完成了几个版本 还不错 下了几万张图 看着成就爽歪歪啊<br/>