# semver-shell
Bash shell script to automate semantic version on ci/cd pipelines

Read version from git tag and update git tag:

```shell
$ ./semver_version.sh
```

Read version from git tag and update git tag and print version to a text file:

```shell
$ ./semver_version.sh -l text -f ./artifacts/version.txt
```

Read version from git tag and don't update git tag and print version to a text file:

```shell
$ ./semver_version.sh -l text -f ./artifacts/version.txt  -o none
```

Read version from git tag and update git tag and print version to a go package named version

```shell
$ ./semver_version.sh -l go -f ./semantic_version/version.go
```

...
