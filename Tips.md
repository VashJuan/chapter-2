nvm install latest https://github.com/coreybutler/nvm-windows?tab=readme-ov-file nvm use
22.1.0

### To update documentation

`npm run compodoc` to regenerate the doc. `compodoc -s` to serve/view the doc at
<http://127.0.0.1:8080/> See <https://compodoc.app/guides/usage.html> and
<https://compodoc.app/> for details

### To update RangerTrak version number

Run `npm run release` per <https://www.npmjs.com/package/standard-version>

This updates bumps the version number in package.JSON & ChangeLog.md by an increment (&
deletes package-lock.json?)

Then run `git push --follow-tags origin main` to publish to Github as a new release

Stage any changes (or add '--allow-empty' to the following), then
`git commit -m "Release-As: 0.11.40"` Some details in service/settings.service.ts &
app.component.ts
<https://github.com/googleapis/release-please#how-do-i-change-the-version-number>

To verify, also check/update package.json & package-lock.json

### To update 3rd party libraries

Commands from Evergreen Angular:

- `npx ng update @angular/core @angular/cdk @angular/cli @angular/google-maps @angular/material`
  (maybe with ' --force' to avoid peer dependency warnings)
- `npx ng update`
- `npx npm-check-updates -u`
- `npm install`

Other useful commands:

- `npm install -g typings` - Looks for updated Typescript type files.
- `npx ng update -g` - Updates global cli & sdk
- `npm install npm@latest -g` - update npm
- `npm install -g typescript` or to update: `npm -g upgrade typescript`; to get version:
  `tsc --version` - update typescript
- `choco upgrade all` - updates https://docs.chocolatey.org/en-us/choco/commands/upgrade
  (requires VSCode being run with Admin permissions) & many apps that use Choclatey
- `https://update.angular.io/?v=15.0-17.0` shows additinoal code updates that may be
  required
- `npm install --save --legacy-peer-deps` - tells NPM to install packages using relaxed V6
  algorithm
- `npm i yarn -g`, then `yarn install` - uses yarn (a nice wrapper for npm)
- `npm outdated` - show availability of newer packages
