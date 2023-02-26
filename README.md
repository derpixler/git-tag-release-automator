# git-release-automator
This script automates Git release tagging and creation of matching release branches for major and minor releases.

The shell script fetch the latest Git tag and prompts the user to increase the major, minor, or patch version. Depending on the user's choice, the script creates a new Git tag and tries to switch to a release branch like "release/v1.1.0". If no release branch is available, the script creates a new release branch based on the new Git tag and pushes it to the remote repository.

```
❯ git-release-automator
Latest tag: v1.1.0
Which part of the version do you want to increase? (M.m.p)
Your choice: p

Switched to existing release branch release/v1.1.0

Git tag v1.1.1 created and pushed successfully.
```

### Install:
```
composer require --prefer-source derpixler/git-release-automator
```

### Execute:
```
./vendor/bin/git-release-automator
 ```

## Contact:

- Name: René Reimann
- Email: info@rene-reimann.de
- LinkedIn: https://www.linkedin.com/in/rene-reimann-18b50a127
- GitHub: https://github.com/derpixler