# Linux













# 小白的成长之路
------------------------------
## 想要执行历史命令可以考虑history

## 命令行历史   
* 保存你输入的命令历史。可以用它来重复执行命令  
* 登录shell时，会读取命令历史文件中记录下的命令~/.bash_history  
* 登录进shell后新执行的命令只会记录在缓存中；这些命令会用户退出时“追加”至命令历史文件中命令行历史  
* 重复前一个命令，有4种方法  
&ensp;&ensp;&ensp;&ensp; 1. 重复前一个命令使用上方向键，并回车执行  
  &ensp;&ensp;&ensp;&ensp; 2. 按 !! 并回车执行  
 &ensp;&ensp;&ensp;&ensp; 3.输入 !-1 并回车执行  
 &ensp;&ensp;&ensp;&ensp; 4.按 Ctrl+p 并回车执行  
* !:0 执行前一条命令（去除参数）  
* Ctrl + n 显示当前历史中的下一条命令，但不执行  
* Ctrl + j 执行当前命令  
* !n 执行history命令输出对应序号n的命令  
* !-n 执行history历史中倒数第n个命令  
  
* !string 重复前一个以“string”开头的命令  
* !?string 重复前一个包含string的命令  
* !string:p 仅打印命令历史，而不执行  
* !$:p 打印输出 !$ （上一条命令的最后一个参数）的内容  
* !*:p 打印输出 !*（上一条命令的所有参数）的内容  
* ^string 删除上一条命令中的第一个string  
* ^string1^string2 将上一条命令中的第一个string1替换为string2  
* !:gs/string1/string2 将上一条命令中所有的string1都替换为 string2  
命令行历史  
* 使用up（向上）和down（向下）键来上下浏览从前输入的命令  
* ctrl-r来在命令历史中搜索命令  
 &ensp;&ensp;&ensp;&ensp;（reverse-i-search）`’：  
* Ctrl+g：从历史搜索模式退出  
* 要重新调用前一个命令中最后一个参数  
 &ensp;&ensp;&ensp;&ensp;!$ 表示  
 &ensp;&ensp;&ensp;&ensp;Esc, .（点击Esc键后松开，然后点击 . 键）   
 &ensp;&ensp;&ensp;&ensp;Alt+ .（按住Alt键的同时点击 . 键）
## 调用历史参数  
* command !^ 利用上一个命令的第一个参数做cmd的参数  
* command !$ 利用上一个命令的最后一个参数做cmd的参数  
* command !* 利用上一个命令的全部参数做cmd的参数  
* command !:n 利用上一个命令的第n个参数做cmd的参数  
* command !n:^ 调用第n条命令的第一个参数  
* command !n:$ 调用第n条命令的最后一个参数  
* command !n:m 调用第n条命令的第m个参数  
* command !n:* 调用第n条命令的所有参数 
* command !string:^ 从命令历史中搜索以 string 开头的命令，并获取它的第一
个参数  
* command !string:$ 从命令历史中搜索以 string 开头的命令,并获取它的最后一
个参数  
* command !string:n 从命令历史中搜索以 string 开头的命令，并获取它的第n
个参数  
* command !string:* 从命令历史中搜索以 string 开头的命令，并获取它的所有
参数
调用历史参数
命令history  
* history [-c] [-d offset] [n]  
* history -anrw [filename]  
* history -ps arg [arg...]  
-c: 清空命令历史  
-d offset: 删除历史中指定的第offset个命令  
n: 显示最近的n条历史  
-a: 追加本次会话新执行的命令历史列表至历史文件  
-r: 读历史文件附加到历史列表  
-w: 保存历史列表到指定的历史文件  
-n: 读历史文件中未读过的行到历史列表  
-p: 展开历史参数成多行，但不存在历史列表中  
-s: 展开历史参数成一行，附加在历史列表后
命令历史相关环境变量  
* HISTSIZE：命令历史记录的条数  
* HISTFILE：指定历史文件，默认为~/.bash_history  
* HISTFILESIZE：命令历史文件记录历史的条数 
 * HISTTIMEFORMAT=“%F %T “ 显示时间  
* HISTIGNORE=“str1:str2*:… “ 忽略str1命令，str2开头的历史  
* 控制命令历史的记录方式：  
环境变量：HISTCONTROL  
ignoredups 默认，忽略重复的命令，连续且相同为“重复”  
ignorespace 忽略所有以空白开头的命令  
ignoreboth 相当于ignoredups,   ignorespace的组合  
erasedups 删除重复命令  
* export 变量名="值“  
* 存放在 /etc/profile 或 ~/.bash_profile  
## -------要想提高速度，掌bash的快捷键是很有必要的
## bash的快捷键  
* Ctrl + l 清屏，相当于clear命令  
* Ctrl + o 执行当前命令，并重新显示本命令  
* Ctrl + s 阻止屏幕输出，锁定  
* Ctrl + q 允许屏幕输出  
* Ctrl + c 终止命令  
* Ctrl + z 挂起命令   
* Ctrl + a 光标移到命令行首，相当于Home  
* Ctrl + e 光标移到命令行尾，相当于End  
* Ctrl + f 光标向右移动一个字符  
* Ctrl + b 光标向左移动一个字符  
*  Alt + f 光标向右移动一个单词尾  
* Alt + b 光标向左移动一个单词首  
* Ctrl + xx 光标在命令行首和光标之间移动  
* Ctrl + u 从光标处删除至命令行首  
* Ctrl + k 从光标处删除至命令行尾  
* Alt + r 删除当前整行   
* Ctrl + w 从光标处向左删除至单词首  
* Alt + d 从光标处向右删除至单词尾  
* Ctrl + d 删除光标处的一个字符  
* Ctrl + h 删除光标前的一个字符  
* Ctrl + y 将删除的字符粘贴至光标后  
* Alt + c 从光标处开始向右更改为首字母大写的单词  
* Alt + u 从光标处开始，将右边一个单词更改为大写  
* Alt + l 从光标处开始，将右边一个单词更改为小写  
* Ctrl + t 交换光标处和之前的字符位置  
* Alt + t 交换光标处和之前的单词位置  
* Alt + N 提示输入指定字符后，重复显示该字符N次  
_**意注**_ ：Alt组合快捷键经常和其它软件冲突

## 获取帮助的能力决定了技术的能力！
------
## 多层次的帮助 
 ### whatis  
### command --help  
### man and info  
### /usr/share/doc/  
### Red Hat documentation  
### 其它网站和搜索 
## whatis
显示命令的简短描述  
使用数据库  
刚安装后不可立即使用  
makewhatis | mandb制作数据库  
使用示例：  
whatis cal 或 man –f cal

## 命令帮助
内部命令：help COMMAND 或 man bash  
外部命令：   
&ensp;&ensp;&ensp;&ensp;（1）COMMAND --help  
        &ensp;&ensp;&ensp;&ensp;COMMAND -h  
         &ensp;&ensp;&ensp;&ensp;（2） 使用手册  
          &ensp;&ensp;&ensp;&ensp;man COMMAND  
          &ensp;&ensp;&ensp;&ensp;（3）信息页  
         &ensp;&ensp;&ensp;&ensp; info COMMAND  
          &ensp;&ensp;&ensp;&ensp;（4）程序自身的帮助文档  
         &ensp;&ensp;&ensp;&ensp;README  
         &ensp;&ensp;&ensp;&ensp; INSTALL  
         &ensp;&ensp;&ensp;&ensp; Changelog  
          &ensp;&ensp;&ensp;&ensp;（5）程序官方文档  
         &ensp;&ensp;&ensp;&ensp; 官方站点：Documentation  
          &ensp;&ensp;&ensp;&ensp;（6）发行版的官方文档  
         &ensp;&ensp;&ensp;&ensp;（7）Google 

## --help和-h选项     
* 显示用法总结和参数列表   
* 使用大多数，但并非所有的  
* 示例：  
date --help  
【】表示可选项  
CAPS或<>表示变化的数据  
...表示一个列表  
x|y|z  的意思是“ x 或 y 或 z “
-abc的 意思是-a -b –c
{} 表示分组
## man命令
* 提供命令帮助的文件  
* 手册页存放在/usr/share/man  
* 几乎每个命令都有man的"页面"
* man页面分组为不同的“章节”  
+ 统称为Linux手册  
+ man命令的配置文件： /etc/man.config |man_db.conf   
&ensp;&ensp;&ensp;&ensp; MANPATH /PATH/TO/SOMEWHERE: 指明man文件搜索位置    
* man -M /PATH/TO/SOMEWHERE COMMAND: 到指定位置下搜索  
COMMAND命令的手册页并显示  
* 中文man需安装包man-pages-zh-CN 

## man 章节
&ensp;&ensp;&ensp;&ensp;1：用户命令  
&ensp;&ensp;&ensp;&ensp;2：系统调用  
&ensp;&ensp;&ensp;&ensp;3： C库调用  
&ensp;&ensp;&ensp;&ensp;4：设备文件及特殊文件  
&ensp;&ensp;&ensp;&ensp;5：配置文件格式  
&ensp;&ensp;&ensp;&ensp;6：游戏  
&ensp;&ensp;&ensp;&ensp;7：杂项  
&ensp;&ensp;&ensp;&ensp;8：管理类的命令  
&ensp;&ensp;&ensp;&ensp;9：Linux 内核API 
## man 帮助段落说明
 帮助手册中的段落说明：  
 1. NAME 名称及简要说明  
2. SYNOPSIS 用法格式说明  
&ensp;&ensp;&ensp;&ensp; • [ ] 可选内容  
&ensp;&ensp;&ensp;&ensp; • <> 必选内容  
&ensp;&ensp;&ensp;&ensp; • a|b 二选一  
&ensp;&ensp;&ensp;&ensp; • { } 分组  
&ensp;&ensp;&ensp;&ensp; • ... 同一内容可出现多次  
3. DESCRIPTION 详细说明  
4. OPTIONS 选项说明  
5. EXAMPLES 示例  
6. FILES 相关文件  
7. AUTHOR 作者
8. COPYRIGHT 版本信息
9. REPORTING BUGS bug信息  
10. SEE ALSO 其它帮助参考

## man帮助  
* 查看man手册页  
&ensp;&ensp;&ensp;&ensp;man [章节] keyword  
* 列出所有帮助  
&ensp;&ensp;&ensp;&ensp;man –a keyword  
* 搜索man手册  
&ensp;&ensp;&ensp;&ensp;man -k keyword 列出所有匹配的页面  
&ensp;&ensp;&ensp;&ensp;使用 whatis 数据库  
* 相当于whatis  
&ensp;&ensp;&ensp;&ensp;man –f keyword  
* 打印man帮助文件的路径  
&ensp;&ensp;&ensp;&ensp;man –w [章节] keyword  
## man命令  
man命令的操作方法：使用less命令实现  
&ensp;&ensp;&ensp;&ensp;space, ^v, ^f, ^F: 向文件尾翻屏  
&ensp;&ensp;&ensp;&ensp;b, ^b: 向文件首部翻屏  
&ensp;&ensp;&ensp;&ensp;d, ^d: 向文件尾部翻半屏  
&ensp;&ensp;&ensp;&ensp;u, ^u: 向文件首部翻半屏  
&ensp;&ensp;&ensp;&ensp;RETURN, ^N, e, ^E or j or ^J: 向文件尾部翻一行 y or ^Y or ^P or k  
or ^K：向文件首部翻一行  
&ensp;&ensp;&ensp;&ensp;q: 退出  
#：跳转至第#行  
&ensp;&ensp;&ensp;&ensp;1G: 回到文件首部  
&ensp;&ensp;&ensp;&ensp;G：翻至文件尾部  

## man搜索  
/KEYWORD:  
&ensp;&ensp;&ensp;&ensp;以KEYWORD指定的字符串为关键字，从当前位置向文件尾部搜索；不区分字符大小写；  
&ensp;&ensp;&ensp;&ensp;n: 下一个  
&ensp;&ensp;&ensp;&ensp;N：上一个  
?KEYWORD:  
&ensp;&ensp;&ensp;&ensp;以KEYWORD指定的字符串为关键字，从当前位置向文件首部搜索；不区分字符大小写；  
&ensp;&ensp;&ensp;&ensp;n: 跟搜索命令同方向，下一个  
&ensp;&ensp;&ensp;&ensp;N：跟搜索命令反方向，上一个  
info  
man常用于命令参考 ，GNU工具info适合通用文档参考  
没有参数,列出所有的页面  
info 页面的结构就像一个网站  每一页分为“节点”  
链接节点之前 *  
info [ 命令 ]  
## 导航info页 
* 方向键，PgUp，PgDn 导航 
* Tab键 移动到下一个链接  
* d 显示主题目录  
* Home 显示主题首部  
* Enter进入 选定链接  
* n/p/u/l 进入下/前/上一层/最后一个链接  
* s 文字 文本搜索  
* q 退出 info


