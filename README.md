# gitBarf

###blehhhhhh goes gitBarf. it spits out the history of a git repo into itself.

Example:
A repo: *foo.git* has two commits. hashes:
* 12345
* 43210

cd foo
ls -> [readme.md]
git status -> [clean]
curl 
chmod +x gitBarf
./gitBarf
ls -> [readme.md, 12345, 43210]
git status -> [untracked: .gitignore]

###gitBarf will NOT wipe your stuff...

cd foo
ls -> [readme.md, 12345]
git status -> [clean]
curl 
chmod +x gitBarf
./gitBarf -> [Nope!]
ls -> [readme.md, 12345]
git status -> [clean]
