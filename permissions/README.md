# Permissions in Linux
- The need for security

Since its inception, Unix was designed to be accessible for multiple users at the same time from different locations. Thus the need for security protocols was born and one of these systems is the ***permissions*** system. This allows system admins and other users to have full control over who controls what in the server.

- Basic commands

Before learning the basic commands we need to get an idea on how permissions are visualised. If you type the command ```ls -l``` in the terminal, you should get a display like this for each file and directory inside the current working directory you are. ![Image](http://linuxcommand.org/images/file_permissions.png)

1. [chmod](http://linuxcommand.org/lc3_man_pages/chmod1.html) - modify file access rights
2. [su](http://linuxcommand.org/lc3_man_pages/su1.html) - temporarily become the superuser
3. [sudo](http://linuxcommand.org/lc3_man_pages/sudo8.html) - temporarily become the superuser
4. [chown](http://linuxcommand.org/lc3_man_pages/chown1.html) - change file ownership
5. [chgrp](http://linuxcommand.org/lc3_man_pages/chgrp1.html) - change a file's group ownership

## Project Permission_Scripting

- In this project we were required to modify permissions using scripts which we practised last week. 

Below you will find a list of the scripts with a short intro on what its function is.

- The Scripts

[0-iam_betty](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/0-iam_betty) (make betty temporary super user)

[1-who_am_i](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/1-who_am_i) (display the info the curret user)

[2-groups](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/2-groups) (display groups that current user is member of)

[3-new_owner](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/3-new_owner) (change permission of file to betty)

[4-empty](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/4-empty) (creating an empty file)

[5-execute](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/5-execute) (change permission of file hello)

[6-multiple_permissions](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/6-multiple_permissions) (change more permissions in hello)

[7-everybody](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/7-everybody) (change permission for all users)

[8-James_Bond](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/8-James_Bond) (change permission as requested)

[9-John_Doe](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/9-John_Doe) (changes permission to file hello -rwxr-x-wx)

[10-mirror_permissions](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/10-mirror_permissions) (mirrors permission from one file to another)

[11-directories_permissions](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/11-directories_permissions) (changes the permissions in a recursive way for current dir and child dir)

[12-directory_permissions](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/12-directory_permissions) (create dir with specific permissions)

[13-change_group](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/13-change_group) (change the group of hello to school)

[14-change_owner_and_group](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/14-change_owner_and_group) (change owner and group of current dir)

[15-symbolic_link_permissions](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/15-symbolic_link_permissions) (change owner and group of symbolic link)

[16-if_only](https://github.com/Katrolli/holbertonschool-shell/blob/main/permissions/16-if_only) (change owner if current owner is a specific name)



