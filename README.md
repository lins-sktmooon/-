# -
代码在Releases里面

实时年龄检测、年龄识别、只需要Python和OpenCV、dlib库就可以运行，方便的很
这个主要在在香橙派5 Pro(Ubuntu20.04)上面运行，也可以在Windows上简单运行


​
system-test.py 该程序只带有摄像头实时识别年龄功能，受光线影响比较大。可以在Windows上运行

all.py 是年龄检测带gpio操控和超声波距离判断。当人体进入到距离摄像头两米的范围时，摄像头将会根据检测到的年龄是否成年，如果成年，则启动电机（gpio电平改变）使其旋转。如果未成年，则不会启动。香橙派5 Pro用。

hc-sr04.py 是超声波识别功能。香橙派5 Pro用。超声波两个接口分别接TRIG_PIN = 27和ECHO_PIN = 26，也就是右下角那两个

contorl-pi5.py 是树莓派5用的，感兴趣的可以试试，但有bug，如果人离开了检测范围程序将会崩溃，但该问题在香橙派5 Pro版本的all.py上已经解决，可以参考all.py的解决方法，其实是多了两个if判断

opencv-acamera.py 用来检测你的摄像头是否正常，也就是打开摄像头画面并显示

gad.py 练模型的

age_deploy.prototxt和age_net.caffemodel是模型文件，同样后缀的也都是

​！！！！注意文件路径！！！！
