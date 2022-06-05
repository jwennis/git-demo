Just testing out some git stuff
#### Create local epository
Navigate to project directory, initialize local repo
```
$ cd "path/to/repo"
$ git init 
$ git status
```
Add all files and commit changes
```
$ git add .
$ git commit
$ git log
```
#### Generate SSH key
check existing keys
```
$ ls -al ~/.ssh
```
generate new key
```
$ ssh-keygen -t rsa -b 4096 -C "email@domain.com"
```
ensure agent is running & add key
```
$ eval $(ssh-agent -s)
$ ssh-add ~/.ssh/id_rsa
```
#### Add key to Github profile
1. copy contents of `~/.ssh/id_rsa/id_rsa.pub`
2. paste it in `https://github.com/settings/keys`
3. Verify key is added properly to authenticate with Github
```
$ ssh -T git@github.com
```
#### Push existing local repo to Github
```
$ git remote add origin https://github.com/jwennis/improved-waffle.git
$ git branch -M main
$ git push -u origin main
```
#### Clone Github repo to local machine
```
$ git clone git@github.com:username@my-repo.git
```