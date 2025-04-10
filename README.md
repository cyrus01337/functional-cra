# Functional CRA (Create React App)

![The definition of "boilerplate"](https://i.imgur.com/0xEmAP6.png)

This is a template repository used to simplify the above, as setting this up for every project adds up overtime.

## Usage

```sh
gh repo create -p cyrus01337/functional-cra --public --clone $(basename $PWD) && \
    gh repo clone $(basename $PWD) . -- --recurse-submodules
```

`.` is the current directory, meaning the project will be generated in the directory this command is
invoked under, whereas omitting the `.` (path) creates a sub-directory and goes through the typical
interactive installation.

Due to my unfortunate (to some) obsession with submodules, the
`--recurse-submodules` Git flag is required to simplify submodule
initialisation.

## Inclusions

- [Prettier](https://prettier.io/) - standard web development formatter

## Plugins

### Prettier

- `@ianvs/prettier-plugin-sort-imports` - auto-sorts imports (better alternative to
  [Trivago's implementation](https://github.com/trivago/prettier-plugin-sort-imports),
  offers much more customisation)
- `prettier-plugin-sort-json` - JSON file formatting, typically for configuration files
