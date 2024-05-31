# GitHub Actions Org level

Common repository for org-level GitHub actions to demonstrate GH Enterprise restriction workaround. Meant to be used as a submodule and pulled recursively.

## Usage

Add actions as modules:

``` shell
git submodule add -- https://github.com/actions/github-script.git actions/github-script
git submodule add -- https://github.com/hashicorp/setup-terraform.git terraform/setup-terraform
git submodule add -- https://github.com/reviewdog/action-tflint.git reviewdog/action-tflint
```

Recommended: use specific tags to maintan stability of your actions

``` shell
git submodule set-branch --branch v7 -- actions/github-script
git submodule set-branch --branch v3 -- terraform/setup-terraform
git submodule set-branch --branch v1 -- reviewdog/action-tflint
```

In your actual repository use it as a submodule

``` shell
git submodule add -- https://github.com/igormedo/org-level-actions.git .github/org-level-actions
```
