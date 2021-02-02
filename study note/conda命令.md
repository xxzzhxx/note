# conda环境使用基本命令

```conda
conda update -n base conda        #update最新版本的conda
conda create -n xxxx python==3.5   #创建python3.5的xxxx虚拟环境
conda activate xxxx               #开启xxxx环境
conda deactivate                  #关闭环境
conda env list                    #显示所有的虚拟环境
conda info --envs                 #显示所有的虚拟环境

```

# 更新，卸载安装包：

```
conda list         #查看已经安装的文件包
conda list  -n xxx       #指定查看xxx虚拟环境下安装的package
conda update xxx   #更新xxx文件包
conda uninstall xxx   #卸载xxx文件包
//pip 也可以
```

# 删除虚拟环境

```
conda remove -n xxxx --all   //删除xxxx虚拟环境
```

# 临时使用豆瓣镜像源

```pip
pip install packagename -i http://pypi.douban.com/simple --trusted-host pypi.douban.com
```

