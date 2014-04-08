mktool
=======

a tool for cocos2dx used to generate makefile

=======

cocos2dx在android机上的编译是需要makefile文件的，而本工具提供一鍵生成makefile文件。<br/>

命令格式：<br/>
python mian.py /Users/xxx/Document/cocos2dx/project/Classes<br/>
python main.py ../Classes<br/>
python main.py D:/cocos2dx/project/Classes<br/>
在没有发生错误的情况下，会在Classes目录下生成一个叫mkfile.mk的文件，在android工程的Android.mk文件下，导入该文件。<br/>
导入mkfile文件：include $(LOCAL_PATH)/../../Classes/mkfile.mk<br/>
导入文件列表：LOCAL_SRC_FILES += $(MY_SRC_FILES)<br/>
导入目录列表：LOCAL_C_INCLUDES := $(MY_SRC_DIRS)
