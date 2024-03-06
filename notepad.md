https://dhenandi.com/easy-ways-to-transfer-your-file-to-file-io/  
All files are encrypted when stored on our servers.  
Or, if you are on CLI mode, you also can upload your file to file.io with this command:  

$ curl -F "file=@/your/folder/file.txt" https://file.io  
{"success":true,"key":"2ojE41","link":"https://file.io/2ojE41","expiry":"14 days"}  
$ curl https://file.io/2ojE41  
This is a test  
$ curl https://file.io/2ojE41  
{"success":false,"error":404,"message":"Not Found"}  
==============================================================================================  
#实战过程中关于阿里云数据库连接问题  
https://forum.90sec.com/t/topic/1872  
正常情况下阿里云一般数据库和网站是分离的，而且一般情况下只能通过网站连接数据库。  
哪怕有时候遇到阿里云数据库是可以连接的，也只是知道内网ip。  
发现一个情况 阿里云的数据库内网连接地址比外网ip地址少两位。  
如果遇到知道内网数据库连接信息，不妨加2位ping一下能通基本上就是外网地址，  
能不能外连就看运气了。  
譬如：rm-wz03dy6e5774ky0gd.mysql.rds.aliyuncs.com 49  
你可以用字典工具生成下(数字+小写字母2位组合字典)：ip.txt  
左边批量添加：rm-wz03dy6e5774ky0gd  
右边批量添加：.mysql.rds.aliyuncs.com  
然后批量ping命令：for /f %d in (ip.txt) do (ping %d -n 1 && echo %d >>通.txt || echo %d >>不通.txt)  
自己去试试自己的阿里云实例吧。  
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++  
通过分析com.android.browser的源码，发现android默认的browser增加cookie是在数据库中增加记录，和window不同，win是采用一个txt文本文件的形式来存储cookie。而android是将cookie存储在数据库中。具体的介绍在《android cookie存储位置》一文中有介绍。我们都知道，android每个应用程序的存储空间都是独立的。不管使用preference还是database存储，都会在每个/data/data/package name/下面进行存储（preference存储在/data/data/package name/shared_prefs/xxxx.xml）。前面也说到cookie是存在数据库中，那么如果采用非浏览器访问网络需要保留cookie的话我们就应该在database中建立cookies表，并且存入相应的cookies数据。    

        
pip uninstall onnxruntime  
pip install onnxruntime==1.14.0  
windows 7 + python 3.8.10 (64bit)  
你可以尝试一下。  
