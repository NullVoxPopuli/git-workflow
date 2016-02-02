# Setting up your Machine
ref: [The Git Setup Guide from GitHub](https://help.github.com/articles/set-up-git/)

Note that anything with the command line *will* be easier with a \*nix machine.

## Install Git

It is recommended against GUI-based git clients, because they hamper learning and will get in the way when something bad happens (merge conflict, bad squash, etc).

| Operating System | Install Via |
| -- | -- |
| Ubuntu | `sudo apt-get install git` |
| Windows | [Download and Install this file](https://git-scm.com/download/win) |
| OS X | [Download and Install this file](http://git-scm.com/download/mac) |

On Windows, this will install a terminal-like program called 'git-bash'.  
Ubuntu and OS X already have terminals, so just the git binary is installed.

## Post-Install Setup

- [Setup your user](https://help.github.com/articles/set-up-git/#setting-up-git)
   - `git config --global user.name "YOUR NAME"`
   - `git config --global user.email "YOUR EMAIL ADDRESS"`

- [Setup your authentication](https://help.github.com/articles/set-up-git/#next-steps-authenticating-with-github-from-git)
  This can either be via SSH Keys or cached username/password. Using SSH is the most seamless way to use git.

  - To Cache your username/password, you may use this command:  
   - `git config --global credential.helper wincred`  
      Leaving out `--global` will apply the command only to the current repository.

  - If you clone using SSH, you MUST use SSH Keys.
    - See [Generating a new SSH key (GitHub)](https://help.github.com/articles/generating-a-new-ssh-key/)
