# 40-tools

## git

### update a forked repo [](https://stackoverflow.com/questions/7244321/how-do-i-update-a-github-forked-repository)

```
# Add the remote, call it "upstream":

git remote add upstream https://github.com/whoever/whatever.git

# Fetch all the branches of that remote into remote-tracking branches

git fetch upstream

# Make sure that you're on your master branch:

git checkout master

# Rewrite your master branch so that any commits of yours that
# aren't already in upstream/master are replayed on top of that
# other branch:

git rebase upstream/master

If you've rebased your branch onto upstream/master you may need to force the push in order to push it to your own forked repository on GitHub. You'd do that with:

git push -f origin master
```
### check, it worked
```
(sds7) rainer@neuron:/media/rainer/_data/30-projects/donkeycar-dev_heavy02011/gym-donkeycar$ git remote -v
origin	https://github.com/Heavy02011/gym-donkeycar.git (fetch)
origin	https://github.com/Heavy02011/gym-donkeycar.git (push)
upstream	https://github.com/tawnkramer/gym-donkeycar.git (fetch)
upstream	https://github.com/tawnkramer/gym-donkeycar.git (push)
```
## docker

### Removing unused Docker objects
```
docker system prune    
```
