# Linux

## SSH
All ssh keys and configurations are stored in `~/.ssh`(~ means users home folder).
If you want to delete or view your ssh keys just check this folder.

### Viewing your ssh keys
```bash
cd ~/.ssh # if you're already at home, just cd .ssh
ls
```
Each ssh key is a pair of public and private keys. They're usually named as:
```
id_[algorithm]
id_[algorithm].pub
```
You can view their content via cat or less:
```bash
cat id_[algorithm].pub
```

### Generating a new ssh key
[Github document on generating ssh keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"

```
### Adding ssh key to github
Go to github/settings/SSH and GPG keys/New SSH key.
```bash
cat ~/.ssh/id_[algorithm].pub
```
paste this content in github.

### Summary
```bash
cd ~/.ssh
ls
ssh-keygen -t ed25519 -C "your_email@example.com" # if you don't already have ssh keys
cat ~/.ssh/id_[algorithm].pub
```
