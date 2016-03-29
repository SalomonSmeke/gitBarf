# gitBarf

gitBarf and its cousin scripts do not need internet access. theyre also poorly behaved children that have not been tested. and 0 thought has been put into them. use at your own risk.

###cleanup in aisle 5!

##blehhhhhh goes gitBarf. it spits out the historical contents of a git repo into itself.

Example:
A repo: *foo.git* has two commits. hashes:
* 12345
* 43210
```bash
cd foo
ls -> [readme.md]
git status -> [clean]
wget https://raw.githubusercontent.com/SalomonSmeke/gitBarf/master/gitBarf
chmod +x gitBarf
./gitBarf
ls -> [readme.md, 12345, 43210]
git status -> [untracked: .gitignore]
```
#####gitBarf will NOT wipe your stuff...
```bash
cd foo
ls -> [readme.md, 12345]
git status -> [clean]
wget https://raw.githubusercontent.com/SalomonSmeke/gitBarf/master/gitBarf
chmod +x gitBarf
./gitBarf -> [Nope!]
ls -> [readme.md, 12345]
git status -> [clean]
```

##sluuuuurp goes barfSlurp. it walks the directories gitBarf made and removes .git directories

Example:
A repo: *foo.git* has been gitBarf'd
```bash
cd foo
ls -> [readme.md, 12345, 43210]
cd 12345
ls -a [.git]
cd ..
./barfSlurp
ls -> [readme.md, 12345, 43210]
cd 12345
ls -a []
```

##wipe wipe goes barfUndo. it removes the directories gitBarf made.

Example:
A repo: *foo.git* has been gitBarf'd
```bash
cd foo
ls -> [readme.md, 12345, 43210]
./barfUndo
ls -> [readme.md]
```
