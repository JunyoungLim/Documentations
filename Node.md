Install `nvm` with https://github.com/nvm-sh/nvm.

You will have `nvm` command ready to use. You can update `nvm` by following the official instruction (either through `curl/wget` or manual `git` pull).

Install `node` and `npm` with:
```bash
nvm install node
nvm install-latest-npm
```

Update 
```bash
npm ls -g --depth=0.
npm update -g
```

Install AWS Amplify with:
```bash
npm install -g @aws-amplify/cli
```

### Resolving package deps
```bash
ncu
```
or
```bash
npm-check-updates
```

Then `ncu - u` to upgrade `package.json` then `npm i` to install the updated packages.
