# git-notes

### **configure git**:
---
- there are three differnet levels in which the configs for git can be managed they are system,user and project level.

- this can be controlled by  providing a `--system` for system wide configurations and `--global` for user specific configurations or not provinding a flag all together from within the root of the repository for project specific configurations.

- In case of project specific configurations the configurations get writern to `.git/config` of the repo.

#### **Set user name:**
- this user name shows up in commits and pull requests

```
git config [--system,--global] user.name USER_NAME
```
#### **Set email address:**
- This email address shows up in commits and pull requrests
```
git config [--system,--global] user.email EMAIL_ADDRESS
```

#### **Set the editor:**
- This setting tells which editor to open when writing a commit message Ex: during a merge

```
git config [--system,--global] core.editor EDITOR_NAME
```

#### **Turn on color mode:**
- Setting this to true adds color to the o/p of various git commands Ex: the git logs

```
git config [--system,--global] color.ui true
```
#### **List all configuration:**

```
git config [--system,--global] --list
```
---

### **Turning on the auto complete feature:**

Head over to [git](https://github.com/git/git) and navigate to `contrib/completion` and download `git-completion.bash` to your computer , make an entry in your `.bashrc` so that the file is sourced  when your shell starts.

