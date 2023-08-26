## anaconda环境问题
查看环境信息： `conda info -e`  
创建一个新环境：`conda create --name 环境名 python=3.7`  
创建环境并添加包：`conda create --name 环境名 包名`  
删除环境：`conda remove -n 环境名 --all`  
切换环境：`conda activate 环境名`  
退出环境：`conda deactivate`  
导出环境中包名：`conda env  export --name 环境名> 导出名.yaml`  
批量安装包：`conda install --yes --file base.txt`  
 
## conda安装包
安装包：`conda install 包名`  
更新一个包：`conda update 包名`  
更新部分包：`conda update numpy scipy pandas `  
更新所有包：`conda update --all`  
卸载包：`conda remove 包名`  
查看安装包：`conda list`  
升级anaconda：`conda update anaconda`  
## conda添加国内镜像源
```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
conda config --set show_channel_urls yes
```
换回默认源
```
conda config --remove-key channels
```
## pip安装包
安装包：`pip install 包名`  
查看需要更新的包：`pip list --outdated`  
更新包：`pip install -U 包名` 或者 `pip install --upgrade 包名`  
卸载包：`pip uninstall 包名`  
查看安装包：`pip list`  
导出环境：`pip list --format=freeze > requirements.txt`  
通过 requirements 文件批量安装包：`pip install -r requirements.txt`  
requirements 文件批量卸载软件包：`pip uninstall -r requirements.txt`  

conda安装包相比于pip安装更加安全，会自动解决包安装的配置问题，但是安装速度相对较慢。

## pip 更换国内镜像源
临时使用： 
可以在使用pip的时候在后面加上-i参数，指定pip源 
```
 pip install scrapy -i https://pypi.tuna.tsinghua.edu.cn/simple
 ```

永久修改： 
linux: 
修改 ~/.pip/pip.conf (没有就创建一个)， 内容如下：
```
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
```
windows: 
直接在user目录中创建一个pip目录，如：C:\Users\xx\pip，新建文件pip.ini，内容如下
```
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
```

## setup更换国内镜像源

方法一：

修改文件 ~/.pydistutils.cfg文件`vim ~/.pydistutils.cfg`为：
```
[easy_install]
index_url = https://pypi.tuna.tsinghua.edu.cn/simple
```
方法二：

直接在setup.py的同目录放置一个setup.cfg：
```
[easy_install]
index_url = https://pypi.tuna.tsinghua.edu.cn/simple
```