**Weekly Recorded Livestreams every Saturday at 0900 PST**

- Read the FAQs
- The Outline
- The Codes of Conduct
- The Discord Announcements

- To get the Badge, you need to have completed 100% stars and pass all of the validators

> If you overuse the GitPod free tier, look to other platforms to complete the coursework or create a new account.

> LocalStack is a local alternative to AWS' Services, **but** you're not actually experiencing the *real* AWS
## Office Hours
- Limit of 100 People
- Bring your technical questions and be able to screen share
- Videos are recorded and shared for paid tier on ExamPro site for viewing later
- Tuesdays @0700 PST/Thursdays @1000 PST and will be posted in the Discord or ExamPro (~1 Hour)
# Preweek Checklist
- [x] AWS Account
- [x] Terraform Cloud Account
- [x] GitHub Account
- [x] GitPod Account
- [x] Clone the GitHub Project Template Repo
- [ ] Configuration AWS CLI (in GitPod)
- [x] Configuration Terraform CLI (in GitPod)
- [x] Get into the Discord (for Support and Graded Tiers)
- [ ] Finish Week-0 (Prep) in ExamPro
- [ ] Finish Week-0 (Project Prep) in ExamPro

# Using GitPod
## Branching
- Use branches to work on new features until ready to merge and to address specific issues.
- `git checkout -b <branch-name>` - When choosing a branch name, try to start it with the issue number and a short reference to the Issue being addressed.
- Once you're ready to commit, start your message with a pound sign, `#`, followed by the Issue number then you can continue with the commit message as normal.
	- This will assign your commit as an addressal to the specified issue.
## Tags

- You can use tags to track your versions in GitHub, `git tag <version>`.
	- After you create the tag, use `git push --tag` to assign the tag to the current branch.
### Semantic Versioning 🧙

The general format: **MAJOR.MINOR.PATH**, eg. `1.0.1`

1. **MAJOR** version when you make incompatible API changes
2. **MINOR** version when you add functionality in a backward compatible manner
3. **PATCH** version when you make backward compatible bug fixes

> Additional labels for pre-release and build metadata are available as extensions to the **MAJOR.MINOR.PATCH** format.

## Bash Scripts
- `chmod u+x <file>` - Modifies the user permissions with the executable permission
- `.sh` or other executable script extensions are not required as they are not *technically* semantically correct and are already defined after the Shebang, `#!`, eg. `#!/usr/bin/env bash`

### Refactoring into Bash Scripts
- Upon initial installation of the Terraform CLI, I noticed an issue with the install requiring user intervention. While troubleshooting, it was found that apt-key was deprecated, as well as, most of the original install commands once I referred to the Hashicorp Install instructions. Instead, I've made a bash script to run all of the necessary Terraform CLI install commands.
	- This keeps the GitPod Task file neat and tidy
	- Allows for an easier time when debugging the install is necessary
	- Makes for better portability for other projects that need to install Terraform CLI.
# Resources 🔗
1. [Install Terraform CLI | Hashicorp](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli) - Used for the Terraform CLI Install commands as the original install instructions were outdated. Terraform made the addition of the gpg keyring.
2. [Oh My Bash | GitHub](https://github.com/ohmybash/oh-my-bash) - Bash CLI Prettify