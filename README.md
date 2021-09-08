# `git-deploy`

Learn more: (link pending)

## Requirements

 * Python 3.7+ (check with `python3 --version`)
 * git 1.8+ (check with `git --version`)
 * A GitHub repo connected to Cloud Build with [source-based deployments](https://cloud.google.com/build/docs/automating-builds/create-manage-triggers)

## Installation

* Clone this repo
* Set the execution bit
    ```
    chmod +x git-deploy
    ```
* Copy `git-deploy` into a place on your `PATH`. 
    ```
    # example location
    cp git-deploy /usr/local/bin
    ```
* Confirm installation by running the script: 
    ```
    cd ~ # a non-git repo
    git deploy
    ```
    * Success: `fatal: not a git repository (or any of the parent directories): .git`
        * The new git extension has been successfully added, but you are not in a git repo, so no action was taken. 
    * Error: `git: 'deploy' is not a git command. See 'git --help'.`
        * The extension is not available. Check your `PATH`. 


## Commands

* `git deploy`: git push, and echo build logs

* `git deploy retry`: manually trigger build, and echo build logs

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for details.

## License

Apache 2.0; see [`LICENSE`](LICENSE) for details.

## Disclaimer

This project is not an official Google project.
