1 注册开源中国的git账号https://git.oschina.net/
2 安装git https://git-scm.com/downloads
3 找到需要提交的项目，右击

![git-bash](http://img.blog.csdn.net/20170228191310945?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
4 在出现的命令行中输入 git init

![git-bash-init](http://img.blog.csdn.net/20170228191544934?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

5  打开Android Studio，进入File--->Settings...--->Version Control--->git,填入刚安装的git的路径，test。
    
    ![git-as-test](http://img.blog.csdn.net/20170228191950596?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

6 将视图切为Project，右击项目--->git--->add

![git-as-add](http://img.blog.csdn.net/20170228192728404?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

如果右击没有git选项，请打开File--->Settings,点击Version Control
![config](http://img.blog.csdn.net/20170228194229443?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

7 VCS--->git--->Commit Directory..
 ![git-c-1](http://img.blog.csdn.net/20170228194628523?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
 出现下图、填写commit message，点击commit and push，过程中出现对话框，一律commit。
 ![git-c-2](http://img.blog.csdn.net/20170228194712773?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
8 之后应当出现下图所示：
![git-p-1](http://img.blog.csdn.net/20170228195025619?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
点击Define remote：
	![git-p-2](http://img.blog.csdn.net/20170228195200468?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
	其中URL填写osc git 上建立的项目url,登陆osc git http://git.oschina.net/，新建项目。
	![git-p-3](http://img.blog.csdn.net/20170228195617184?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
	
9 填入url，ok，出现下图所示：

![git-p-4](http://img.blog.csdn.net/20170228195810794?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
设置密码的先填密码，之后会出现：
![git-p-5](http://img.blog.csdn.net/20170228200018559?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

 10 之后，会发现无法push,这是因为云上托管的代码与本地不一致所致，先pull,再push，如果无法pull，右击项目目录打开git-bash，输入：
git pull origin master --allow-unrelated-histories         假设本地源是origin，分支是master。无法push，请先解决conflict，即修改冲突文件，commit，再push。
完

![over](http://img.blog.csdn.net/20170228202030508?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc3VtbWVyX3NhbWE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

注：
1. [git无法pull仓库refusing to merge unrelated histories ](http://blog.csdn.net/lindexi_gd/article/details/52554159)
2. [Git下的冲突解决](http://www.cnblogs.com/sinojelly/archive/2011/08/07/2130172.html)
