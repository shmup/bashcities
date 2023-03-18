# bashcities

[![AUR](https://img.shields.io/badge/AUR-install-blue)](https://aur.archlinux.org/packages/bashcities)
[![Chat](https://img.shields.io/badge/chat-join-green)](https://tatsumoto-ren.github.io/blog/join-our-community.html)
![GitHub](https://img.shields.io/github/license/tatsumoto-ren/bashcities)

> A neocities client that actually works.

```
$ bashcities -h

Usage: bashcities [OPTION] [FILE]

A Neocities client written in Bash.

Options:
-h, --help     display this help text and exit
-V, --verbose  verbose mode
-p, --profile  specify the desired profile name
-n, --no-git   don't use git to list files
init NAME      create a new profile with NAME
push           upload all files that differ from the remote
status         lists all files that differ from the remote
list           print all remote files
list --local   print all local files
download       download a backup of the site
upload FILE    upload a file
delete FILE    delete a file from the remote

bashcities home page: https://github.com/tatsumoto-ren/bashcities
```

## Workflow example

Below is my current workflow. Basically I do some some stuff, commit it, then push with bashcities.

You can get your api key from https://neocities.org/settings 🠒  manage site settings 🠒  api key.

```
    bashcities init ezpz          # (creates ~/.config/neocities/ezpz)
    vim ~/.config/neocities/ezpz  # (edit the api_key and site_directory)
    cd ~/site_directory
    echo wazzup > index.html
    git init; git add index.html; git commit -m "Show how this thing works"
    bashcities -p ezpz push
```

Full README available at: https://github.com/tatsumoto-ren/bashcities#bashcities
