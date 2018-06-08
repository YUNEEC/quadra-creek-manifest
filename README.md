# Quadra Creek manifest

Manifests for Quadra Creek releases and development

## Prerequisite

### Git repo

> Repo is a tool that we built on top of Git. Repo helps us manage the many Git repositories, does the uploads to our revision control system, and automates parts of the Android development workflow. Repo is not meant to replace Git, only to make it easier to work with Git in the context of Android. The repo command is an executable Python script that you can put anywhere in your path.

#### Install

```
$ curl https://storage.googleapis.com/git-repo-downloads/repo -o ~/bin/repo
$ chmod +x ~/bin/repo
$ export PATH=~/bin:$PATH
```

For China mainland use tsinghua mirror instead

```
$ curl https://mirrors.tuna.tsinghua.edu.cn/git/git-repo -o ~/bin/repo
```

## Initialize the Git repository

`default.xml` - manifest for Quadra Creek development

```
$ repo init -u https://github.com/YUNEEC/quadra-creek-manifest.git
```

By default repo tries to fetch repo tools from Google, for China mainland use `--repo-url` to override the repo url with tsinghua mirror:

```
$ repo init -u https://github.com/YUNEEC/quadra-creek-manifest.git --repo-url=https://mirrors.tuna.tsinghua.edu.cn/git/git-repo/
```

## Download the codes

```
$ repo sync
```

## FAQ

* What if `curl: (22) The requested URL returned error: 404 Not Found Server does not provide clone.bundle; ignoring.` happens?
  Can be safely ignore.
