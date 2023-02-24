# git-release-automator
This script automates Git release tagging and creation of matching release branches for major and minor releases.

The shell script fetch the latest Git tag and prompts the user to increase the major, minor, or patch version. Depending on the user's choice, the script creates a new Git tag and tries to switch to a release branch like "release/v1.1.0". If no release branch is available, the script creates a new release branch based on the new Git tag and pushes it to the remote repository.

```
❯ ./git-release-automator.sh
Latest tag: v1.1.0
Which version number do you want to increase? (M.m.p)
Your choice: p

Switched to existing release branch release/v1.1.0

Git tag v1.1.1 created and pushed successfully.
```

## Usage:

- Clone the repository and navigate to the script directory
- Run the script using "./git-release.sh" command
- The script will fetch the latest Git tag and prompt the user to increase the major, minor, or patch version
- Based on user input, the script will create a new Git tag and try to switch to a release branch like "release/v1.1.0"
- If no release branch is available, the script will create a new release branch based on the new Git tag and push it to the remote repository.

## Note:

- This script requires Git to be installed on the system.
It is recommended to run the script in a Git repository to avoid errors.
  
## Contact:

- Name: René Reimann
- Email: info@rene-reimann.de
- LinkedIn: https://www.linkedin.com/in/rene-reimann-18b50a127
- GitHub: https://github.com/derpixler