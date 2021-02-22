# git&github的使用

1. git的简介

   代码管理，版本控制工具

   可回退，相当于备份管理的一个工具

   linux之父发明的一个东西

2. git安装

   ![image-20210221203820373](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221203820373.png)

   全部默认选项即可（安装路径可自己选择）

   右键出现下面两个选项即安装成功

   ![image-20210221204111757](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221204111757.png)

3. 初始化git文件夹（每换一个工作目录都要初始化）

   打开项目文件夹，然后右键Git Bash Here

   这个文件夹会存放我们代码的备份文件，备份到.git文件夹中

   ```git
   git init
   ```

4. 配置个人信息（只需要配置一次）

   就是在git中设置一下当前使用的用户是谁（在初始化的文件夹里进行配置）

   global表示全局配置，这个操作只需要完成一次即可以了

   ```git
   git config --global user.name "learnlog"
   #配置用户名，输入后无任何反应即表示成功
   ```

   ![image-20210221210009177](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221210009177.png)

   ```
   git config --global user.email "1277590830@qq.com"
   #配置邮箱，输入后无任何反应即表示成功
   ```

   ![image-20210221210206424](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221210206424.png) 

5. 把代码存储到git仓库中

   1.  提交

       ![image-20210221211332108](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221211332108.png)

       

      ```
      git add ./readme1.md
      #输入后无任何反应即表示成功
      ```

       ![image-20210221211512582](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221211512582.png)

       

   2. 拖入

       ![image-20210221211636699](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221211636699.png)

      ```
      git commit -m "我们完成了第一个功能！"
      #把大门口的东西全部拖入房间，需要记录拖入的说明，必须登记一下
      ```

      ![image-20210221211914792](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221211914792.png)

       

       ![image-20210221212051976](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221212051976.png)

6. 提交新版本（重复五的步骤）

    如果没有修改过文件又提交的话：

   ![image-20210221213212760](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221213212760.png)

   ```
   git add ./readme1.md
   ```

   ```
   git commit -m "XXX说明"
   ```

   ![image-20210221212826121](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221212826121.png)

   ```
   #强制退出
   1.--ESC
   2.--:q!
   ```

7. 查看状态

    查看是放在大门口还是已经拖入房间了

   ```
   git status
   ```

    ![image-20210221213804369](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221213804369.png)

    出现modified说明已经放入大门口，接下来应该把它拖入房间中

    ![image-20210221213916558](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221213916558.png)

    ![image-20210221213942629](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221213942629.png)

    修改文件直接git status

    ![image-20210221214058575](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221214058575.png)

    红色表示只改代码，没有执行命令

    把刚修改的东西改回去，相当于没有做出任何改变

    ![image-20210221214420427](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221214420427.png) 

8. 添加其他文件

    ![image-20210221214834682](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221214834682.png)

   ![image-20210221214846776](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221214846776.png)

    ![image-20210221214939535](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221214939535.png)

    两处报红，需要把这两个都进行命令处理

   ```
   git add ./
   #./表示当前目录，这个命令表示会把当前目录的所有修改的文件都放入大门口
   ```

    ![image-20210221215232315](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221215232315.png)

    提交命令不需要指定文件名，这个命令是把大门口的文件全部拖入房间

    ![image-20210221215340451](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221215340451.png)

    直接放入房间

    ![image-20210221215606368](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221215606368.png)

    

   ```
   git commit --all -m "这是一次性的操作"
   #把所有修改过的代码一次性放入房间
   ```

    ![image-20210221215737543](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221215737543.png)

    

9. 查看日志（视频也是第九个）

    git清屏操作：clear(直接输入)

    查看提交了几次

   ```
   git log
   ```

    ![image-20210221220313012](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210221220313012.png)

    这是按照时间轴来记录的
   
    
   
   ```
   git log --oneline
   #精简提交记录信息（简洁版日志）
   ```
   
    ![image-20210222164500944](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222164500944.png)
   
    
   
10. 版本回退

     

    ```
    git reset --hard Head~0
    #0是指当前的最近的一次提交的那个文件
    ```

     ![image-20210222165212398](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222165212398.png)

     ![image-20210222165405745](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222165405745.png)

     ![image-20210222165453344](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222165453344.png)

     ![image-20210222165535826](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222165535826.png)

     ![image-20210222165606711](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222165606711.png)

     ![image-20210222165840136](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222165840136.png)

     ![image-20210222165904837](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222165904837.png)

     ![image-20210222165932094](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222165932094.png)

    ​	

11. 通过版本号切换版本

      ![image-20210222170340178](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222170340178.png)

      提交次数过多，无法准确判断回退到哪个版本，可以通过回退版本号方式，直接回退到相应版本

     ```
     git reset --hard de6dd2a 
     ```

      ![image-20210222170606965](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222170606965.png)

      ![image-20210222170631885](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222170631885.png)

      ![image-20210222170736988](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222170736988.png)

      通过标识号进行版本回退

      ![image-20210222170818622](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222170818622.png)

      会出现一个问题，回退之后查看日志，看不到之前的标识号了怎么办？

      

     ```
     git reflog
     #可以看到所有提交过的版本号
     ```

      ![image-20210222171418640](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222171418640.png)

     所有版本的记录都会记录在这里面，需要哪个版本号，直接选取即可

12.  创建分支，切换分支

      master（主线）

     项目还没完成，只完成一部分，如果提交到master，别人拿到代码运行会出错。所以需要分支，对未完成的代码进行管理

     ![image-20210222182623624](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222182623624.png)

      

      ![image-20210222182852077](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222182852077.png)

      别人只能拿master里面的，如果要让别人可以拿分支里面的，需要将分支与主线合并

      ![image-20210222183015916](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222183015916.png)

      

     ```
     git branch dev
     #没有任何反应，即操作成功,dev为分支名称
     git branch
     #查看分支
     ```

      ![image-20210222183224788](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222183224788.png)

      *表示当前所在的位置，即现在所在master

      

     ```
     git checkout dev
     #切换到dev分支
     ```

      ![image-20210222183408252](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222183408252.png)

      ![image-20210222183545258](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222183545258.png)

      ![image-20210222183807895](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222183807895.png)![image-20210222183754178](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222183754178.png)

      ![image-20210222183858030](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222183858030.png)

      切换回master![image-20210222184004637](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222184004637.png)

      ![image-20210222184053035](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222184053035.png)

      切换回master，里面并没有出现分支的文件记录

      把主线和分支合并

     ```
     git merge dev
     #把分支合并到主线中
     ```

      ![image-20210222190717190](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222190717190.png)

      ![image-20210222190753224](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222190753224.png)

      在刚创建时dev里面的东西和master是一样的

13. 合并分支时

     ```
     git branch -d dev
     #删除分支
     ```

      ![image-20210222191629805](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222191629805.png)

      报错，因为，当前正处于dev中，造成无法删除

     ![image-20210222191720640](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222191720640.png)

      切换回master，然后删除分支，即可删除成功

      ![image-20210222191757014](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222191757014.png)

      ![image-20210222191825324](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222191825324.png)

      ![image-20210222191907059](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222191907059.png)

      ![image-20210222192033762](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222192033762.png)

      ![image-20210222192146127](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222192146127.png)

     合并 发生冲突，需要手动解决冲突。处理后，还需要提交一次

14. push命令

      团队协同完成一个项目，共享同一份代码

      ![image-20210222193145258](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222193145258.png)

      服务器：Github（这个网站充当了服务器的功能）

      ![image-20210222193326121](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222193326121.png)

      提交代码到github上：

      github需要一个仓库来和本地的.git相对应

     1.  新建一个仓库

         ![image-20210222193905613](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222193905613.png)

         

     2. 仓库创建完成后

         ![image-20210222193954501](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222193954501.png)

    ​    

     3. 复制HTTPS的链接

         ![image-20210222194111631](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222194111631.png)

         

        ```
        git push https://github.com/Learninglogs/testgit.git master
        ```

         把本地的master分支，上传到服务器上的master分支中，做到一一对应

15. pull命令

      需要输入用户名及密码，我的上传失败，这个问题待解决

      

16. 通过ssh上传代码

      ![image-20210222195804112](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222195804112.png)

      不需要输入用户名及密码

      公钥，私钥，两者之间是有关联的

      生成公钥和私钥

     ```
     ssh-keygen -t rsa -C "1277590830@qq.com"
     ```

      ![image-20210222200206280](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222200206280.png)

      ![image-20210222200306557](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222200306557.png)

      ![image-20210222200435182](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222200435182.png)

      ![image-20210222200534647](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222200534647.png)

      打开公钥，然后复制

      ![image-20210222200637649](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222200637649.png)

      ![image-20210222200749145](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222200749145.png)

      ![image-20210222200856554](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222200856554.png)

      

     ```
     git push git@github.com:Learninglogs/testgit.git master
     ```

      ![image-20210222201234372](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222201234372.png)

      ![image-20210222201253250](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222201253250.png)

      ![image-20210222201554633](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222201554633.png)

      ![image-20210222201607714](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222201607714.png)

      ![image-20210222201638637](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222201638637.png)

      ![image-20210222201724559](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222201724559.png)

     ![image-20210222202252495](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222202252495.png)

      ![image-20210222202326558](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222202326558.png)

      ![image-20210222202348803](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222202348803.png)

      ![image-20210222202430402](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222202430402.png)

      ![image-20210222202800723](C:\Users\12775\AppData\Roaming\Typora\typora-user-images\image-20210222202800723.png)

17. 模拟两个用户push和pull操作

      

