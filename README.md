
*** a simple revision of config file for Aliyun OSSyncone tool ***
***  中文安装请看后面说明   ***
*** Installation Method   ***
a) make sure your linux have python installed. and you need to install python python-pip as well.
for ubuntu/debian/linuxmint use

$sudo apt-get install python-pip

b) Quick Installation method :

you can simply download Ossyncone.7z and unzip to your path by dwonload Ossynccone.7z and run
$7z x Ossyncone.7z

Now everything is ready and you can start to modify config/setting.py according to your OSS account(Region,Access ID and KEY).

***other installation mehtod- Installation procedure with orignal project file***
If you try to respect original contributor, you can pull all original files from https://github.com/lanbaba/Ossyncone/archive/master.zip
extract Ossync master.zip, remove config/setting.default.py 
And download this setting.py to put it in config folder
modify it to use your own access key. For those OSS server are not in Shanghai, you also need to modify "HOST" with your region according to  https://help.aliyun.com/document_detail/31834.html

Now you can run installation ,then everything is done.

安装指南：
１ 安装 python, python-pip, 一般linux都带有python了，debian/ubuntu等只需
sudo apt-get install python-pip

2 下载本项目下打包好的Ossync.7z并解压到任意目录，
修改setting.py，把HOST改成你对应的地区，参考：https://help.aliyun.com/document_detail/31834.html,　并且用您自己的access key 和设置您的bucket和备份目录映射。并用您自己的access id和access key

3 安装
$ sudo python setup.py

5.开始一次备份
$nohup python ossync.py >/dev/null 2>&1 &

成功
