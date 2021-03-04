# Lerna micro cheat sheet

## Initialize lerna monorepo

```bash
# install lerna globally
npm i -g lerna
# create a new dir for project
mkdir awesome-boilerplate && cd awesome-boilerplate
# initialize a new lerna managed repository
lerna init
```

## Create a package

```bash
# create library directory and cd inside
mkdir -p packages/validator && cd packages/validator
# initialize library with scope name
npm init --scope=awesome-boilerplate --yes
```

## Add package as a dependency

```bash
# Add validator library as a dependency to frontend
lerna add @awesome-boilerplate/validator --scope=@awesome-boilerplate/frontend
```

```javascript
import { isNullOrWhitespace } from '@awesome-boilerplate/validator';
```
