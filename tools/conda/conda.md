# Conda Cheat Sheet

## Environment Management

### Creating a new environment
`conda create --name <env_name>`

### Create an environment from a YAML file
`Create an environment from a YAML file`

### Export an environment to a YAML file
`conda env export > <yaml_file>`
`conda env export --from-history  --name env > environment.yml`

### Clone an environment
`conda create --name <new_env_name> --clone <existing_env_name>`

### Activate an environment
`conda activate <env_name>`

### Deactivate the current environment
`conda deactivate`

### Remove an environment
`conda env remove --name <env_name>`

## Package management
### Install a package
`conda install <package_name>`

### Install a specific version of a package
`conda install <package_name>==<version>`

### Install a package from a specific channel
`conda install -c <channel_name> <package_name>`

### Update a package
`conda update <package_name>`

### Remove a package
`conda remove <package_name>`

### List all installed packages in the current environment
`conda list`

### List all installed packages in a specific environment
`conda list -n <env_name>`

### Search for a package
`conda search <package_name>`

## Miscellaneous

### Update Conda
`Update Conda`

### Update all packages in the current environment
`conda update --all`

### Show information about the current environment
`conda info`

### Show information about a specific environment
`conda info -e -n <env_name>`

### Show the path to the current environment
`conda info --envs`

