
### Create an Alias for `git add` and `git commit`

Run this command in your terminal:


`git config --global alias.ac '!git add -A && git commit -m'`

### How It Works:

- `git alias.ac` → Defines a new alias called `ac`
- `!git add -A && git commit -m` → Runs `git add -A` (adds all changes) and `git commit -m` (commits with a message)

### Usage:

Now you can commit changes quickly like this:


`git ac "Your commit message here"`

### **Basic Aliases**


`git config --global alias.s "status -s" git config --global alias.co "checkout" git config --global alias.br "branch" git config --global alias.cm "commit -m" git config --global alias.st "status" git config --global alias.df "diff"`

- `git s` → Short status
- `git co` → Checkout a branch
- `git br` → List branches
- `git cm "message"` → Commit with a message
- `git st` → Show status
- `git df` → Show diff

### **Log & History Aliases**


`git config --global alias.lg "log --oneline --graph --all --decorate" git config --global alias.last "log -1 HEAD"`

- `git lg` → Pretty log with branches
- `git last` → Show last commit

### **Branching & Merging Aliases**


`git config --global alias.rb "rebase" git config --global alias.cp "cherry-pick" git config --global alias.mg "merge"`

- `git rb` → Rebase
- `git cp` → Cherry-pick
- `git mg` → Merge

### **Push & Pull Aliases**

`git config --global alias.p "push" git config --global alias.pl "pull" git config --global alias.fpush "push --force"`

- `git p` → Push
- `git pl` → Pull
- `git fpush` → Force push

### **Fix Mistakes Quickly**

`git config --global alias.undo "reset --soft HEAD~1" git config --global alias.unstage "reset HEAD" git config --global alias.fix "commit --amend --no-edit"`

- `git undo` → Undo last commit (keeps changes)
- `git unstage <file>` → Unstage a file
- `git fix` → Amend last commit without changing the message

