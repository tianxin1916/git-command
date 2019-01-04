# git怎么去操作连接github
1. 前期准备
   - 1.安装git ，官网地址：https://git-scm.com/
   - 2.注册github账号
   - 3.配置github密钥
       - 下载及安装好git后，右击桌面，找到git Bash Here，
       - 打开输入：ssh-keygen-t rsa -C 你的邮箱
       - 一直下一步
    - 打开本地文件，找到.ssh的目录，点进去会有个id_rsa.pub文件，用记事 - 本打开，复制里面内容
    - 在github点击头像的下拉框，settings点进去，找到SSH and GPG keys点击，再点击New SSH key
    - Title随便写，key就把在id_rsa.pub文件里复制的内容粘贴到里面就行了，点击Add SSH key就大功告成了！
    
### 拉取
 - 先在本地新建一个文件夹；进入当前创建的文件夹，终端台输入：git init，则文件夹中会出现一个.git的文件夹
 - 在github点加号里面的new repository创建一个仓库
 - 进入填写名称，说明，勾选Initialize this repository with a README,
 - 在点击Create repository点击确认创建仓库。
 - 然后在本地新建文件夹里面打开终端台输入git clone url（指mark项目的地址）
 - 完成之后项目就被克隆在本地仓库里了。

### 提交项目到github
 - 进入项目目录，再在当前目录放入要放入的项目
 - 执行：git add .
 - 执行：git commit -m “提交项目的说明文字”
 - 执行：git remote add origin url(mark仓库的地址) 让本地仓库与远程仓库关联
 - 执行：git push origin master 本地仓库的代码提交到github上

### 创建分支，提交到分支再合并
 - 执行： git branch test 创建一个test的分支
 - 执行： git checkout test 切换到test分支mark本地仓库上添加新的需要上传的代码
 - 执行：git add .
 - 执行：git commit -m “提交项目的说明文字”
 - 执行：git remote add origin url(github仓库的地址) 让本地仓库与远程仓库关联
 - 执行：git push origin master 本地仓库的代码提交到github上