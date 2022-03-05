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
#### **List all configurations:**

```
git config [--system,--global] --list
```
---

### **Turning on the auto complete feature:**

Head over to the git repository for git [git](https://github.com/git/git) and navigate to `contrib/completion` and download `git-completion.bash` to your computer , make an entry in your `.bashrc` so that the file is sourced  when your shell starts.

---

### **Viewing the git logs:**
- The git logs contains the commit history of the repository. The git log command can be used to explore it

#### **view only last n commits**

```
git log -NUMBER_OF_COMMITS_TO_SHOW
```
example: `git log -3` will show information about the last three commits

#### **View commits made by a particular author:**

```
git log --author=AUTHOR_NAME
```

#### **View commits between a given time range:**
```
git log --since=START_DATE --until=END_DATE
```
**NOTE**: The date should be in `yyyy-mm-dd` format.

#### **View commits which matches a given regex:**
```
git log --grep=REGEX
```

#### **View the contents which changed in this commit:**
```
git log -p
```
#### **View only the commits associated with a given file:**
```
git log FILE_NAME
```

#### **View only the commit ids and a short description:**
```
git log --oneline
```

#### **View the commits represented as a graph:**
```
git log --graph
```

**NOTE**: The `--no-pager` global option can be added to prevent git from piping its output to `less` by default.

#### **View the contents of a specific commit:**
```
git show COMMIT_SHA
```
---
### **Using git diff:**
- `git diff` can be be used to find what changed between two commits , it can also be used to get the difference between two branches.

#### **Get the difference between two commits:**
```
git diff COMMIT_ONE..COMMIT_TWO
```

**NOTE**: different commits can be accessed in refrence to a given commit by adding the `^` sign at the end of the commit or by using the `~NUMBER_OF_COMMITS_TO_MOVE_DOWNWORDS` syntax , it sould also be noted that the commit which refers to the tip of a branch can be accessed using the `HEAD` keyword.

**EXAMPLE**: given a commit hash `commitOne` then `commitOne^` refers to the parent of `commitOne` and `commitOne^^` refers to the grant parent of `commitOne` the same can be achived using the `~` sytax as well, in which the grant parent is referenced by `commitOne~2`.

#### **Get the difference between two branches:**
```
git diff BRANCH_ONE..BRANCH_TWO
```

**NOTE**: use the `--color-words` flag to get information about what exactly changed on each line.

---

### **The three tree architecture:**

![three tree architecture](three-tree-architecture.png "Title")

