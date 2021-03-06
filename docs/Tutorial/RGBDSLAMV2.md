
# RGBD SLAM v2

这次跑得是视觉SLAM的经典程序:RGBD SLAM V2,本实验是一个比较经典的实验,可以建成一个稠密三维点云.所用摄像头是Xtion 2;   
结合半闲居士的SLAM实战和HandsFree的机器人实现.[原文链接](http://www.cnblogs.com/gaoxiang12/p/4462518.html)

## 环境配置
前提仍然是ubuntu14.04,和高博的不同,我用的是indigo,所以在下载程序的时候,我下载的是indigo版本,也就是在github上选择branch,换成indigo,在[github](https://github.com/felixendres/rgbdslam_v2/tree/indigo)
上查看如何安装,或者直接在终端执行下面的命令:

```
//创建工作空间
source /opt/ros/indigo/setup.bash
mkdir -p ~/rgbdslam_catkin_ws/src
cd ~/rgbdslam_catkin_ws/src
catkin_init_workspace
cd ~/rgbdslam_catkin_ws/
catkin_make
echo "~/rgbdslam_catkin_ws/devel/setup.bash"

//下载源码
cd ~/rgbdslam_catkin_ws/src
wget -q http://github.com/felixendres/rgbdslam_v2/archive/indigo.zip
unzip -q indigo.zip
cd ~/rgbdslam_catkin_ws/

//安装
rosdep update
rosdep install rgbdslam
catkin_make
```

#运行程序
直接roslaunch官方包中的launch是不行的,图片信息和没有对应上,还有摄像头的某个服务没有开启,rgbdslam这个节点接受不到照片信息.   
所以我们对文件进行了改动,并放在了handsfree_bringup中,所以,请先启动摄像头
>roslaunch handsfree_bringup openni_slam.launch   

然后启动RGBDSLAM v2的GUI界面
>roslaunch handsfree_bringup rgbdslam_v2.launch

![RGBDSLAM GUI](/images/Tutorial/RGBDSLAM_v2/rgbdslam_v2.jpg)

程序运行良好,就是我的笔记本不太给力...   
可以摁空格暂停查看点云,也可以在全屏之后的上端菜单栏选择需要保存的信息.
