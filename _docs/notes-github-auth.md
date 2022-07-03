Create repo on github, then push up using **ssh** credentials
```bash
git remote add origin git@github.com:dsriseah/urpsys.git
git branch -M main
git push -u origin main
```
Github Create New Account...
Github [create ssh key authentication](https://docs.github.com/en/enterprise-cloud@latest/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
```bash
cd ~/.ssh
ssh-keygen -t ed25519 -C "sri.nutmoon@@yahoo.com"
eval "$(ssh-agent -s)"
ssh-add --apple-use-keychain ~/.ssh/dsriseah-github-ed25519
```
add this entry to `~/.ssh/config`
```
Host github.com-dsriseah
  HostName github.com
  User git
  PreferredAuthentications publickey
  IdentityFile /Users/dsri/.ssh/dsriseah-github-ed25519
  UseKeychain yes
  AddKeysToAgent yes
```

helpful?

`ssh-add -D` deletes all identities cached
`ssh-add -l` lists all the current identities

opening keychain and deleting entries can help too

The general thing that seemed to work was making sure that the User was `git` after I changed to the ssh-style authentication instead of what was in the sourcetree entries. Giving the host a different name might have helped too
Once you reconnect, the cached entreis are restored
