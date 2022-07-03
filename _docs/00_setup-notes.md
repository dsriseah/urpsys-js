# SPECIFICATIONS

* nodejs environment
* build stack: webpack5+babel+(typescript+eslint) creating bundle
* build cli: nodejs+npm scripts+utils
* module system: ESM for node and browser, if possible
* devserver: programmatic webpack
* appserver+ur+services: nodejs+express+ws
* demoserver: electron host appserver+ur+services

# STREAM OF CONSCIOUSNESS LOG

> Mac: install required [xcode command line tools](https://docs.brew.sh/Common-Issues) and [Node Version Manager](https://github.com/nvm-sh/nvm) (`nvm`).

Create the repo folder in Terminal.
```bash
mkdir urpsys
cd urpsys
# install required node+npm via node version manager (nvm)
nvm install v16.15.1
echo v16.15.1 > .nvmrc
nvm use
# initialize git repo
git init --initial-branch=main
```
Add `package.json` to be the working directory
```json
{
  "name": "@dsricomp/urpsys",
  "description": "Sri's Universal 'Ractive Play System (URPSYS)",
  "version": "1.0.0-alpha.1",
  "author": "DSri Seah",
  "license": "MIT",
  "workspaces": [
    "urp_packages/*"
  ]
}
```
Add `.editorconfig`
```
root = true
[*]
indent_style = space
indent_size = 2
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = false
```
Add `.gitignore`
```
# list file globs for git to ignore
node_modules/
```

