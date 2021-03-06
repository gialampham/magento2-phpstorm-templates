# Contribute

## Fork and Install this project

**IMPORTANT:** Before you do this, make sure PhpStorm is not running, or it will overwrite the changed files before shutting down.

1.- Clone this repo.

```
git clone https://github.com/nntoan/magento2-phpstorm-templates.git
```

2.- Personal Comments configuration

```
cd magento2-phpstorm-templates
cp Preferences/fileTemplates/includes/nntoan_variables.txt.dist Preferences/fileTemplates/includes/nntoan_variables.txt
vim Preferences/fileTemplates/includes/nntoan_variables.txt
```

3.- Set Symlinks to new templates:

**OS X**

```
ln -s $(PWD)/Preferences/templates/* ~/Library/Preferences/<product name><version number>/templates/
ln -s $(PWD)/Preferences/fileTemplates/2M* ~/Library/Preferences/<product name><version number>/fileTemplates/
ln -s $(PWD)/Preferences/fileTemplates/includes/* ~/Library/Preferences/<product name><version number>/fileTemplates/includes/
ln -s $(PWD)/Preferences/fileTemplates/internal/* ~/Library/Preferences/<product name><version number>/fileTemplates/internal/
```

**Linux**

```
ln -s $(PWD)/Preferences/templates/* ~/.<product name><version number>/config/templates/
ln -s $(PWD)/Preferences/fileTemplates/2M* ~/.<product name><version number>/config/fileTemplates/
ln -s $(PWD)/Preferences/fileTemplates/includes/* ~/.<product name><version number>/config/fileTemplates/includes/
ln -s $(PWD)/Preferences/fileTemplates/internal/* ~/.<product name><version number>/config/fileTemplates/internal/
```

## Create new Templates

### Live templates:

0. Add new live templates on PHPStorm within the ***ToanMagento2*** group.
0. Commit, push and create PR

### File Template:

0. Create new File template on PHPStorm
0. Copy this template from your local PHPStorm preferences into this project `Preferences/fileTemplates`
0. Commit, push and create PR

### Update Live templates Documentation

`cd magento2-phpstorm-templates/Preferences/templates && echo 'cat //templateSet/template/@name' | xmllint --shell "ToanMagento2.xml"`
