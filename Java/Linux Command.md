## Linux  Command

* cp命令
  * cp -r 
  * cp -p
  * cp -a
* mv命令
  * mv [选项] 源文件 目标文件（重命名）
  * mv [选项] 源文件 目录 （复制）
* rm命令
  * rm -f ：删除文件不提示
  * rm -r：删除目录/文件夹（递归删除）
* 通配符
  * *：匹配多个字符
  * ?：匹配一个字符

#### 文本查看命令

* cat：查看并且连接文件 
  - cat  a.txt b.txt：先显示`a.txt`的全部内容，然后紧接着显示`b.txt`的全部内容。
  - cat -n：显示文件内容时，同时为每一行添加行号
* head：查看文件的前面n行
  * head a.txt：默认查看a.txt文件的前面10行  
  * head -n 5 a.txt：查看a.txt文件的前面5行  

* tail：
  * tail -f .txt：实时监控文件，当文件有修改的时候把内容打印出来
* wc：
  - wc -l .txt：统计行数
  - wc -w .txt：统计字符数
  - wc -c .txt：统计字节数

#### 解压缩和打包

* tar：打包
  * tar c ：打包 
  * tar x：解包
  * tar xf：解包成一个文件 
  * tar zxf：将一个gzip压缩后的包解压
  * tar jxf：将一个bzip2压缩后的包解压
  * tar xf /xx/xx.tar.   -C  /path：把包解包到一个路径下的文件中 
  * tar cf：打包成一个文件 
  * ls -lh：可以查看文件的大小，以M兆的形式显示 
* gzip：压缩（速度更快）
  * tar czf：打包并压缩--->.tar.gz
* bzip2：压缩（体积更小）
  * tar cjf ：打包并压缩 --->.tar.bz2
* 常用扩展名
  * .tar.gz：打包后用gzip压缩
  * .tar.bz2：打包后用bzip2压缩
  * .tgz：.tar.gz的缩写 
  * .tbz2：.tar.bz2的缩写 

#### 文本编辑器vi和vim

* 文本编辑器的四种模式
  * 正常模式
    * 注意：如果是对一整行进行操作，就会在当前光标的下一行生效。如果是对一行的部分进行操作，就会在当前光标的后面位置生效。
    * 复制、粘贴
      * yy：复制一整行
      * n yy：代表复制n行
      * y $：复制从光标位置到结尾的位置
      * p：粘贴到光标所在的下一行 
    * 剪切
      * dd：剪切一整行
      * d$：剪切从光标位置到行尾
      * n dd：剪切n行
    * 撤销
      * u：撤销上一步的操作
      * ctrl+r：取消上一次撤销操作
    * 删除
      * x：按下x删除光标所在位置的字符 
      * r：按下r键，再输入字符，光标所在字符被替换成新输入的字符。
    * 光标的移动
      * 上下左右键
      * HJKL：左下上右
      * n+G：快速移动到指定行
      * g：移动到文本第一行
      * G：移动到文本最后一行
      * ^：移动到这一行的行首
      * $：移动到这一行的行尾
  * 插入模式
    * 进入插入模式
      * 光标的位置进入并输入：按小写i
      * 光标这行的开始进入并输入：按大写I
      * 光标后面的一个位置进入并输入：按小写a
      * 光标这行的结尾进入并输入：按大写A
      * 光标这行的下一行进入并输入：按小写o
      * 光标这行的上一行进入并输入：按大写O
    * 文本内容输入
  * 命令模式
    * 输入set nu：显示文本编辑器中的行
  * 可视模式
  * 模式之间的切换
    * 如何进入正常模式：输入vi，默认进入的是正常模式。
    * 正常模式-----》插入模式：按下i，下方显示插入模式
    * 插入模式-----》正常模式：按下ESC
    * 正常模式-----》命令模式：按下:冒号键，输入w，q等命令
    * 命令模式-----》正常模式：按下ESC
* 操作
  * 输入vi/vim：相当于挡开了记事本
  * 输入vi/vim 文件名：相当于用记事本打开了一个文件 

#### grep命令（使用正则表达式在文本中进行全局搜索并打印匹配的内容。）

- options
  - -i：忽略大小写
  - -v：输出非正则匹配的内容
  - -n：显示行号
  - -r：递归搜索
- 正则表达式
