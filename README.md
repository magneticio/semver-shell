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

To trigger a major release use "[major]" keyword in your git commit message.
Ex:

```
Add new feature abc [major]
- line 1
- line 2
```

Currently multiline messages merged into one line in the release command.
For minor releases use "[minor]"
Default release type is patch

Build versions and pre-releases are not supported.
