# MAC常用命令

标签（空格分隔）： mac shell

---
- git打印漂亮的日志
```
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --"
```
- ssh生成
```
git config --global user.name "yikwing"
git config --global user.email "hubeieasy@gmail.com"

ssh-keygen -t rsa -C "hubeieasy@gmail.com"
```
- ZSH autojump配置
```
[[ -s $(brew --prefix)/etc/profile.d/autojump.sh ]] && . $(brew --prefix)/etc/profile.d/autojump.sh

j --stat
```
- 显示隐藏mac finder文件
```
display dialog "隐藏/显示隐藏文件" buttons {"可见", "隐藏"} with icon 2 with title "Switch to presentation mode" default button 1

set switch to button returned of result

if switch is "隐藏" then
	do shell script "defaults write com.apple.finder AppleShowAllFiles -bool false;
KillAll Finder"

else
	do shell script "defaults write com.apple.finder AppleShowAllFiles -bool true;
KillAll Finder"

end if
```
- 显示Mac安全来源
```
sudo spctl --master-disable
```



