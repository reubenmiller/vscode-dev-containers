# Getting started

This repository contains some tools to help with thin-edge.io development, for example a dev container configuration which contains everything you need to build/run the project.

## Using the dev container

1. Clone this project

    ```
    git clone https://github.com/reubenmiller/vscode-dev-containers.git
    ```

2. Get the path to the project

    ```sh
    echo "$(pwd)/vscode-dev-containers/repository-containers"
    ```

3. Add the local folder path (from the previous step) to your VSCode configurations

    ```jsonc
    {
        // ... your existing settings.json details

        "dev.containers.repositoryConfigurationPaths": [
            "/Users/myuser/vscode-dev-containers/repository-containers/"
        ]
    }
    ```

4. You can close your `vscode-dev-containers` folder now.

5. Clone the project you want to work with (the repo should match that of what is inside `vscode-dev-containers/repository-containers/github.com/<owner>/<repo_name>`)

6. Open the VSCode command pallet, then type/select `Dev Containers: Rebuild and Reopen in Container`

    If everything works properly the correct `.devcontainer` folder from the `vscode-dev-containers/repository-containers` folder will be selected.

    If it does not work, then double check that owner and repo name is set correctly to your project by inspecting the `.git/config` file. For more information about this VSCode feature checkout the [online documentation](https://code.visualstudio.com/remote/advancedcontainers/configure-separate-containers)

# References

* https://code.visualstudio.com/remote/advancedcontainers/configure-separate-containers
