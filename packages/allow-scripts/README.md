# @lavamoat/allow-scripts

a tool for only running dependency lifecycle hooks specified in an allowlist


### configure

configuration goes in `package.json`
```json
{
  "lavamoat": {
    "allowScripts": {
      "keccak": true,
      "core-js": false
    }
  }
}
```

automatically generate a configuration (that skips all lifecycle scripts) and write into `package.json`. edit as necesary.
```sh
npx allow-scripts auto
```

### disable scripts

disable all scripts by default inside `.yarnrc` or `.npmrc`
```
ignore-scripts true
```

### run

run all lifecycle scripts for packages specified in `package.json`
```sh
npx allow-scripts
```

### debug

prints comprehension of configuration and dependencies with lifecycle scripts
```sh
npx allow-scripts list
```
