[![GitHub tag (latest SemVer)](https://img.shields.io/github/tag/derpixler/git-tag-release-automator.svg?label=latest%20version&color=brightgreen)](https://github.com/derpixler/git-tag-release-automator/releases) [![PowerShell](https://img.shields.io/badge/PowerShell-Windows%20%7C%20macOS%20%7C%20Linux-blue)](https://github.com/powershell/powershell)
 [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) [![Downloads](https://img.shields.io/badge/Downloads-6k-orange)]([https://npmjs.com/package/package-name](https://github.com/derpixler/git-tag-release-automator))



# :rocket: Save time with the Git-Tag-Release-Automator!
If you are a friend of [git flow](https://www.atlassian.com/de/git/tutorials/comparing-workflows/gitflow-workflow) and use tagging in your release flow, I'm sure you struggle with manually determining the latest git tag and then creating a matching release branch is a tedious task. What if there was a way to automate this process to save time, effort and errors?

__This script automates:__ 
* 🥇 Release tagging
* 🥇 Matching release branch creation for major and minor releases
* 🥇 prevent you for create tags with no relevant changes


__The shell script:__ 
* 🎂 Provieds an init action,
* 🎊 Fetch the latest Git tag,
* 🚑 Prompts the user to increase the major, minor, or patch version, 
* 📽️ Fetch the last tag depending on the user's choice,
* 👾 Check if there a exiting release branch like "release/v1.1.0" based on the new tag,
* 🥇 Validate changes in the release branch, before a new tag will pushed, 


### Install:
```
composer require derpixler/git-tag-release-automator
```

### Execute:
```
./vendor/bin/git-tag-release-automator
 ```
 
### Create a new tag command in action
```
❯ ./vendor/bin/git-tag-release-automator
Latest tag: v1.1.0
Which part of the version do you want to increase: Major (M), Minor (m) or Patch (p)? (M.m.p)
Your choice: p

Switched to existing release branch release/v1.1.0

Git tag v1.1.1 created and pushed successfully.
```

## Some Insights

### Initial setup for new projects.
```
❯ ./vendor/bin/git-tag-release-automator
There are no existing tags. Do you want to create a tag starting with 'v'? (y/n)
Your choice: y

No "release/v1.0.0" found, create one? (y/n)
Your choice: y

Release branch "release/v1.0.0" created.
Now you can merge into "release/v1.0.0" and create tags.
```

### Create new tag but there is no matching release branch.
```
❯ ./vendor/bin/git-tag-release-automator
Latest tag: v1.4.1

Which part of the version do you want to increase: Major (M), minor (m) or patch (p)?
Your choice: m

No "release/v1.5.0" found, create one? (y/n)
Your choice: y

Release branch "release/v1.5.0" created.
Now you can merge into "release/v1.5.0" and create tags.
```

### Create new minor version tag.
```
❯ ./vendor/bin/git-tag-release-automator
Latest tag: v1.4.1

Which part of the version do you want to increase: Major (M), minor (m) or patch (p)?
Your choice: m

Git tag v1.5.0 created and pushed successfully.
```


### Create new patch version tag
```
❯ ./vendor/bin/git-tag-release-automator
Latest tag: v1.5.0

Which part of the version do you want to increase: Major (M), minor (m) or patch (p)?
Your choice: p

Git tag v1.5.1 created and pushed successfully.
```

## 🤙 Contact:

- Name: René Reimann
- Email: info@rene-reimann.de
- LinkedIn: https://www.linkedin.com/in/rene-reimann-18b50a127
- GitHub: https://github.com/derpixler
