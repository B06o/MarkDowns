## total
git globally config -> ssh key generation/ssh-agent/ssh-add -> add public key on github.com -> ssh config github.com proxy


```
# git start
git config --global --list
git config --global user.name [ur name]""
git config --global user.email [ur email]""
```


## ssh key

```

# -t encryption
// ssh-keygen -t rsa -C "ur email" [filename]
ssh-keygen -t rsa -C [filename]


# start ssh-agent
# win
# server: start -> settings -> applications -> check functions -> ssh server
  # find openssl xxxxx in service

ssh-add [file path]
```


## pub key on github.com

```
github public key

```


## test connection

```
ssh -T git@github.com
```


## ssh config

config ssh config
activate the config file while tunnel to github.com
filepath on win: */user/.ssh/config 

```

Host github.com
  User git
  Port 22
  Hostname github.com
  IdentityFile "C:\Users\ASUS\.ssh\gitKey"
  TCPKeepAlive yes

Host ssh.github.com
  User git
  Port 443
  Hostname ssh.github.com
  IdentityFile "C:\Users\ASUS\.ssh\gitKey"
  TCPKeepAlive yes
```
