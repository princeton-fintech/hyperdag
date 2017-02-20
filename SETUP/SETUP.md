# Dev Setup

## Getting `git` and your GitHub account configured

1. Check that you have `git` installed by running `which git`. If it returns a non-empty
path, then it is installed. You an also verify this by running `git --version` which should
return a non-empty version (i.e. 2.3.2). 

2. If `git` is not installed, then run `xcode-select --install` to install the XCode Command
Line Tools (which includes `git` as well as other useful dev tools such as `gcc`, etc.).

Note: The following assumes that you have a GitHub account tied to an email address. If you
don't, go right now to [GitHub.com](http://github.com) and sign up for an account with an email
address you check frequently. Also, send your username to 
[rahulmehta@princeton.edu](mailto:rahulmehta@princeton.edu) so you can be added to the Princeton 
FinTech organization.

3. Configure `git` with your GitHub profile info
    1. Set your name by running `git config --global user.name "<your_name>"`. Be sure to wrap
       it in quotes
    2. Set your email to the email address that you used to create your GitHub account. run 
       `git config --global user.email <your_github_email@example.com>`

4. Add an SSH key to GitHub
    1. Check if you have an existing SSH keypair by running `cat ~/.ssh/id_rsa.pub`. If that
    file does not exist/is empty, then there is no existing keypair for `git` to use. If there
    is an existing keypair, check if there is an email address at the end of the public key. If
    it is different than the email tied to your GitHub account, then delete `id_rsa.pub` and `id_rsa`
    from the `~/.ssh` directory and follow the next steps to regenerate it. If you have a key that 
    has the correct email, skip to step c.
    2. Run `ssh-keygen -t rsa -b 4096 -C "your_github_email@example.com"` to begin generating a new keypair.
    Say yes to the default location (`$HOME/.ssh/`), and optionally add a password (you will need to enter
    this password every time the SSH key is used).
    3. Add the new SSH key to your GitHub account by following the instructions here: https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/


## Dev Environment/Stack
Coming soon...