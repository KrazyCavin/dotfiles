dotfiles
========

The sweet sweet home of my lovely dotfiles :honey_pot:

## How to configure

You may or may not notice that there are some variables `%variable%` in dotfiles. For example, in `zshrc`:

```
export GITREPO="%gitrepo%"
```

Because some settings can be different on different machines (directories, shortcuts, term colors...). To make it more flexible, the value of variable can be defined in a `yaml` file, the format looks like:

```
<filename1>:
    <variable1>: <value1>
    <variable2>: <value2>

<filename2>:
    <variable1>: <value1>
    <variable2>: <value2>
```

For example, in `dotfile-config.yaml`:

```
zshrc:
    gitrepo: \/home\/kevinthebest\/git
    comment: ''
    othersource: ~\/.czshrc

i3wm/config:
    comment: ''
```

## How to build

```
./build.sh <yaml_config_file>; source ~/.zshrc
```

The final fines will be generated in `output` folder. Pay attention to create symbol link to the target files in `output` folder.

:heart: