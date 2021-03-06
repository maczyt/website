# Getting Started

## Installation

SAO is a CLI library written in JavaScript, so you can install it from npm:

```bash
npm i -g sao
```

Alternatively, a lot of you may use Yarn instead:

```bash
yarn global add sao
```

Then try the command `sao` in your terminal, if everything works fine you'd see the CLI usages.

## Using Generator

```bash
sao nm my-project
```

By running this command, SAO will install a generator which in this case is [sao-nm](https://npm.im/sao-nm) from npm, and use it to generate files into `my-project` directory.

If you want it to generate into current directoy, just omit the second argument like this: `sao nm`.

A generator could be one of:

- __Local directory__, e.g. `sao ./path/to/my-generator`
- __An npm package__, e.g. `sao react` will be package `sao-react`.
  - To use an npm package that does not follow the `sao-*` naming convention, just prefix the name like this: `sao npm:foo`, then this will use the `foo` package instead of `sao-foo`.
- __A git repository__, e.g. `sao egoist/sao-nm` will use `github.com/egoist/sao-nm`, you can use following prefixes for other git providers:
  - `gitlab:` For GitLab.
  - `bitbucket:` For BitBucket.

## Sub generators

A generator might have sub generators, you can run them like this:

```bash
sao nm:donate
```

The part after `:` is a sub generator called `donate`, by running this command SAO will run the sub generator which will add a `postinstall` script to show donation URL in your `package.json`.
