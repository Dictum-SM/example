# Example DSM Managed Repo

This repo is a non-functional example of git submodule usage and structure  
of a DSM managed environment.

# Design Notes

Everything is intended to be modular:

1. Kustomize from generalized k8s configs that are imported as submodules
2. Use Terraform modules from imported submodules
3. Ansible tasks and roles are intended to be imported as submodules
4. The DSM is a submodule.
5. All submodules should reference tagged release commits.
6. `.state` references resources relative to the repo root.

Utils are special:

1. Utils might not make sense to add as submodules.
2. Utils are mostly exclusive to the respective environment.