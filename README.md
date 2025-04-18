# dxlog - a DNAnexus log reader

[![PyPI - Version](https://img.shields.io/pypi/v/dxlog.svg)](https://pypi.org/project/dxlog)

This app allows for the displaying of latest DNAnexus jobs in a convenient UI.

## Installation

To install the package, you can run the following command.

```console
pip install dxlog
```

However, please be aware, you need to enter your DNAnexus credentials before using the app (in order to access to your projects remotely).

```console
dx login
```

> By default, your information expires in 30 days, but this can be changed using the `--timeout` option.

If you have access to several projects on DNAnexus, you need to choose the specific one for which you wish to see the logs.
Please use `dx select` to do so.

## Usage (from command line)

The most basic way to use the app is the following, which will display the last 100 jobs run on the project.

```bash
dxlog
```

However, the app has 4 options:

* `-p [str]` specifies the project for which you wish to say the jobs (default Current)
* `-u [str]` specifies the user of which you wish to see the jobs (default All)
* `-n [int]` specifies the number of jobs to display when you first open the app (default 100)
* `-s [int]` specifies the incrementation of the number of jobs displayed (default 100)

## Features

Multiple features have been added to the app:

* Show only `done`, `running` or `failed` jobs
* Search for string in job name, user name or date
* Download job output
* Open the job's monitor page

## License

`dxlog` is distributed under the terms of the [MIT](https://spdx.org/licenses/MIT.html) license.
