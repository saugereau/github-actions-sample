# Sample of github actions

## generate changelog 

Based on 
- [github_changelog_generator](https://github.com/github-changelog-generator/github-changelog-generator)
- [ad-m/github-push-action@master](https://github.com/ad-m/github-push-action)

On following git workflow :
- push a branch releases/*
- this will trigger a github action generating changelog on this branch and commit it with user action@github.com
- you just have to merge this branch

## generate github release

Based on 
- [softprops/action-gh-release@v1](https://github.com/softprops/action-gh-release)

The aim here is to reuse generated changelog to fill github release (but only the current release)
On following git workflow :
- tag your master branch with a v*
- this will trigger a github action taking the latest elements of changelog
- create a release with tag name and last element of changelog

