这样就很明白了，访问此站点时，如果域名不是 blog.cncounter.com ,那么就会跳转到 http://blog.cncounter.com/，个人恶意推测,即便你将CNAME文件的内容设置为 www.baidu.com 也是可行的，这样访问的时候直接跳转到百度了。
但是，如果 http://blog.cncounter.com/ 是空的怎么办?  这就需要你自己保证咯。
当然，要是这么结束掉，那本文就是一篇坑文。 
如果你持有这个域名，那么你可以将域名的对应记录也CNAME到 "renfufei.github.io" . 记住， renfufei.github.io 已经是一个互联网上能明确定位到的地址，所以DNS记录完全可以映射到此路径.

例如如下的记录， DNS中，A记录那就是直接指定一个IP。 CNAME就是重命名，指向另一个域名。 主机记录就是前缀，例如: blog, 与 cncounter.com 拼接在一起就是 blog.cncounter.com ，如果你想映射 www.cncounter.com ，那么主机记录就是 www ,记录类型是CNAME，记录值是renfufei.github.io；如果想将 http://cncounter.com 这个根域名也映射到，那么记录类型也是CNAME,主机记录就是一个英文的 at: "@". 你可以将多个域名都映射到 xxxxx.github.io 之类的你自己的站点上，但原则上都会跳转到你新建的 CNAME文件中的域名上。【放心，不会死循环。。。】.好的，恭喜你!
