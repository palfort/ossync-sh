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

$ rm -rf config/setting.default.py

3 download setting.py from this project and put in in Ossync's config path.
modify it to use your own access key

4 run Ossync installation

5 start one time backup

done

