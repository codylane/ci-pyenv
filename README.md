# ci-pyenv
A bash wrapper for python development projects to initialize pyenv in a CI environment

Usage
-----

# Prep

```
git clone git@github.com:codylane/ci-pyenv.git .ci
rm -rf .ci/.git
```

* All further commands assume that you are in your project root, relative to the `.ci` directory.


# Initalize a new virtualenv

* This creates a virtualenv project named `my-special-proejct`
* With python `2.7.15`

```
sed -i.bak -e 's/%%PROJECT_NAME%%/my-special-proejct/g' -e 's/%%PROJECT_PYTHON%%/2.7.15/g' .ci/enable-pyenv
.ci/init-pyenv
```
