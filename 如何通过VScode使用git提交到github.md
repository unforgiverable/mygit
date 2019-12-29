    

#  如何通过VScode使用git提交至给github

  1、首先在github创建一个仓库来放项目
     （1）点击头像-->new repository-->起名字
   2、创建完成后，任意新建一个空文件夹,我是新创了myproject文件夹
        打开文件夹，右键点击git bash
        输入命令：git init     //初始化
           ![](https://img-blog.csdnimg.cn/20191228230752323.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191228230915208.png)
   在文件夹里生成了一个隐藏文件.git
   //如果没有隐藏文件，打开我的电脑，点击组织，打开文件夹和搜索选项，点击查看，把选中显示隐藏文件就可以了
   ![在这里插入图片描述](https://img-blog.csdnimg.cn/20191228231353179.png)
 
   3、用VScode打开文件夹，在里面我创建了名为test.js的文件、
   在git输入以下的命令：
   （1）git add test.js
    （2）git commit -m "第一次练习"
     （3）git remote add origin  https://github.com/unforgiverable/firstrepostory.git

            https://github.com/unforgiverable/firstrepostory.git
              是你仓库的地址，在刚刚创建的库中可以发现
   （4）git push -u origin master    //提交到你的仓库
     ![在这里插入图片描述](https://img-blog.csdnimg.cn/20191228232638145.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMTcyNzc0,size_16,color_FFFFFF,t_70)
     4、在github上设置ssh key
      (1)设置git 的用户名和邮箱
         名字随意起
         ![在这里插入图片描述](https://img-blog.csdnimg.cn/2019122823340657.png)
         检查是否存在ssh key
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191228233518801.png)
如图
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191228233704353.png)
如果没有ssh key,则要生成一下
输入命令 （自己设置的邮箱号）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191228234042683.png)
下面生成的说明中in后面是你的取密钥地址
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191228234143526.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMTcyNzc0,size_16,color_FFFFFF,t_70)
5、获取ssh key
输入命令: cat id_rsa.pub
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191228234538528.png)
打开github ,点击头像，选择settings,选择SSH and GPG keys,点击new SSH key新建一个SSH key，爸之前获取的密钥粘贴进去，添加就好了。
6、验证是否成功设置SSH key
命令： ssh -T git@github.com
显示如下则成功
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191228235206476.png)
