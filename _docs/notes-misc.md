sidenotes on publishing packages using a [package spec](https://docs.npmjs.com/cli/v8/using-npm/package-spec):

* local folder to default registry: `npm publish ./packages/package_name` (use `unpublish` to remove)
* preview what files are packages using `npx npm-packlist`, ignoring files found in `.npmignore` || `.gitignore`, or including only files in `files:` field of `package.json`
* make a tarball: use `npm pack`.

sidenotes on [scoped packages](https://docs.npmjs.com/cli/v8/using-npm/scope):