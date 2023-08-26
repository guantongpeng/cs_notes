## anaconda环境问题
查看环境信息： conda info -e
创建一个新环境：conda create --name 环境名 python=3.7
创建环境并添加包：conda create --name 环境名 包名
删除环境：conda env remove --name 环境名
切换环境：conda activate 环境名
退出环境：conda deactivate
导出环境中包名：conda env  export --name 环境名> 导出名.yaml
批量安装包：conda install --yes --file base.txt
 
## conda安装包
安装包：conda install 包名
更新一个包：conda update 包名
更新部分包：conda update numpy scipy pandas 
更新所有包：conda update --all
卸载包：conda remove 包名
查看安装包：conda list
升级anaconda：conda update anaconda
## pip安装包
安装包：pip install 包名
查看需要更新的包：pip list --outdated
更新包：pip install -U 包名 或者 pip install --upgrade 包名
卸载包：pip uninstall 包名
查看安装包：pip list
导出环境：pip list --format=freeze > requirements.txt
通过 requirements 文件批量安装包：pip install -r requirements.txt
requirements 文件批量卸载软件包：pip uninstall -r requirements.txt

conda安装包相比于pip安装更加安全，会自动解决包安装的配置问题，但是安装速度相对较慢。