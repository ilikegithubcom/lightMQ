步骤：

1、添加空的头文件

lightMQ\socketx\include\sys\stropts.h

2、安装glog

下载：https://code.google.com/archive/p/google-glog/downloads)，

$ ./configurate

$ make

$ sudo make install

3、添加LD_LIBRARY_PATH

$ vi ~/.bashrc

添加export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib

关闭重启Teminate

4、编译socketx

$ cd lightMQ/socketx

$ make clean

$ make

5、编译lightMQ

$ cd lightMQ

$ make clean

$ make

6、启动PubSubSys

打开虚拟机vm1

$ ./PubSubSys [port]

7、启动SubscriberClient

打开虚拟机vm2

$ ./SubscriberClient [server ip] [port]

8、启动PublisherClient

打开虚拟机vm3

$ ./PublisherClient [server ip] [port]

9、vm2订阅消息

打开虚拟机vm2

$ sub userlogin

10、vm3发布消息

打开虚拟机vm3

$ pub userlogin Jenny