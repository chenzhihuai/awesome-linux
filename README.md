| name     | comment                                        |
|----------|------------------------------------------------|
| bat      | a color-full highlighted alternative to cat    |
| xonsh    | a python-style shell to replace bash           |
| lunarvim | an awesome text editor                         |
| intellij | a modern tmux                                  |
| zsh      | a better alternative to bash                   |
| ranger   | a file browers like vim                        |
| pget     | a script to install software without sudo [^1] |
| proxychains | use proxy temporarily [^2]                  |
| sslocal  | a cmdline version of shadosocks [^3]           | 


tips: .profile vs .bashrc
|      | non-login   | login        |
|------|-------------|--------------|
| user | ~/.bashrc   | ~/.profile   |
| all  | /etc/bashrc | /etc/profile |


[^1]: add ~/.apt/usr/bin to $PATH and ~/.apt/usr/lib to `$LD_LIBRARY_PATH`, maybe some other directory.
[^2]:
[^3]: see shadowsocks.json 

tips: user file
| file        | note     | format                                    |
|-------------|----------|-------------------------------------------|
| /etc/passwd | user     | username:password:uid:gid:info:home:shell |
| /etc/group  | group    | group:password:gid:user1,user2,...        |
| /etc/shadow | password |                                           |

linux file permission
```
-rw-r--r-- 12 linuxize users 12.0K Apr  28 10:10 file\_name
|[-][-][-]-   [------] [---]
| |  |  | |      |       |
| |  |  | |      |       +-----------> 7. Group
| |  |  | |      +-------------------> 6. Owner
| |  |  | +--------------------------> 5. Alternate Access Method
| |  |  +----------------------------> 4. Others Permissions
| |  +-------------------------------> 3. Group Permissions
| +----------------------------------> 2. Owner Permissions  
+------------------------------------> 1. File Type: regular file (-), directory (d), symblic (l)
```

about `s` flag:
- on directory's group triplet: New file inherits this directory's group id instead of current user's group id.
- on file: When the setuid or setgid flags are set on an executable file, the file is executed with the file’s owner and/or group privileges.
