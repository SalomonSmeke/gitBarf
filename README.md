# gitBarf

##blehhhhhh goes gitBarf. it spits out the history of a git repo into itself.

Example:
A repo: *foo.git* has two commits. hashes:
* 12345
* 43210
```bash
cd foo
ls -> [readme.md]
git status -> [clean]
curl https://raw.githubusercontent.com/SalomonSmeke/gitBarf/master/gitBarf
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
curl https://raw.githubusercontent.com/SalomonSmeke/gitBarf/master/gitBarf
chmod +x gitBarf
./gitBarf -> [Nope!]
ls -> [readme.md, 12345]
git status -> [clean]
```

##sluuuuurp goes barfSlurp. it walks the direcotries gitBarf made and removes .git directories

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
´´´

##wipe wipe goes barfUndo. it removes the directories gitBarf made.

Example:
A repo: *foo.git* has been gitBarf'd
```bash
cd foo
ls -> [readme.md, 12345, 43210]
./barfUndo
ls -> [readme.md]
´´´