Use the `npm -w` (with) option to specify what package you are manipulating.

* add **new package** to workspace: `npm init -w ./packages/package_folder`
* add **package dependency** to another workspace package: `npm install package_spec -w ./packages/package_folder`

To use project scopes, the `--scope=` flag
* `npm init --scope=@dsri -w ./packages/package_folder`
*  `npm install @dsri/package_folder  -w ./packages/package_folder`

Running scripts:
* run script with `--workspace=package` to specify package(s): `npm run test --workspace=package_folder`
* use `--workspaces` to run the script on all: `npm run test --workspaces`