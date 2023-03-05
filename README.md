# id-card-recognition
可能遇到的问题：
1.No module named 'imutils' ,'cv2'
打开Anaconda Prompt 以管理员身份运行
输入pip install -i https://mirrors.aliyun.com/pypi/simple/ imutils
2.the following arguments are required: -i/--image, -t/--template
pycharm—>运行->编辑配置   在形参里输入--image images/credit_card_01.png --template ocr_a_reference.png
3.ref_,refCnts,hierarchy=cv2.findContours(ref.copy(),cv2.RETR_EXTERNAL,cv2.CHAIN_APPROX_SIMPLE)
not enough values to unpack (expected 3, got 2) 报错
原因是在新版的OpenCV中返回的是两个参数，而在旧版的使用的是三个参数，所以导致错误的发生，所以在解决这个问题时就需要把OpenCV的版本降低
这是网上的方法，我也去查了如何降低opencv的版本，使用了pip install 之类的，还尝试试了创建虚拟环境的办法，但是都没有成功。
事实上，操作很简单，只要换个python解释器就可以了，换成3.7版本，再去指定opencv的版本，安装需要的软件包。
