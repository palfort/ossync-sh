# ossync-sh
modified config file for oss server in shanghai
Please pull all original files from https://github.com/lanbaba/Ossyncone/archive/master.zip
Because of Aliyun OSS DNS change you have to do some modification about the "HOST" and also import necessary python os module.
Replace HOST with your OSS server's place if your OSS is not in Shanghai.

Installation procedure:

1 make sure your linux have python installed. and you need to install python python-pip as well.
for ubuntu/debian/linuxmint use

$sudo apt-get install python-pip

2 extract Ossync master.zip, remove config/setting.default.py 

$rm -rf config/setting.default.py

3 download setting.py from this project and put in in Ossync's config path.
modify it to use your own access key. For those OSS server are not in Shanghai, you also need to modify "HOST" with your region according to  https://help.aliyun.com/document_detail/31834.html

4 run Ossync installation

5 start one time backup

done

安装指南：
１ 安装 python, python-pip, 一般linux都带有python了，debian/ubuntu等只需
sudo apt-get install python-pip

2 下载原始的OSSync软件　https://github.com/lanbaba/Ossyncone/archive/master.zip，并解压，删除config/setting.default.py

3 下载本项目的setting.py ,并放到config目录下，注意您仍要修改setting.py，把HOST改成你对应的地区，参考：https://help.aliyun.com/document_detail/31834.html,　并且用您自己的access key 和设置您的bucket和备份目录镜像

4 安装
$ sudo python setup.py

5.开始一次备份
$nohup python ossync.py >/dev/null 2>&1 &

成功
