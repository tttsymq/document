
### PHP







-----
~~~
1.在桌面创建一个新的文件夹practice: mkdir /Users/username/Desktop/parctice
2.更改practice文件的权限 chmod 755 /Users/username/Desktop
3.进入apache的根目录中 cd 
4.创建一个project文件夹 mkdir project
5.更改该文件夹的权限 sudo chown username:staff project
6.进入该文件件下 cd project
7.建立一个通往桌面的软连接: ln -s /Users/username/Desktop/practice .
8.在桌面的practice文件夹中写一个test.php文件,在浏览器中打开 http://localhost/project/test.php
