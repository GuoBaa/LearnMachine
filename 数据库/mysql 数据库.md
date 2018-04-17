———————————————2018-1-31—————————————-——

学习内容：查看数据库|API
查看当前数据库： SELECT DATABASE() FROM DUAL;

遇到的坑：
当前数据库使用：Post.all ，是总是报错 （JSON::ParserError）。

拆解/总结：

上面坑1的原因：之前使用的Post的字段content，使用的是string存取的数据。后来测试将content的格式变成了序列化的hash，于是读取all的时候会遇到JSON::ParserError的错误。
在使用store之后，原字段的存储只能使用hash结构中已有的key。

———————————————2018-1-31—————————————-——





