# cartwheel : gst-plugins-bad

Intel developer staging area for upstream patch contributions to [gst-plugins-bad](https://gstreamer.freedesktop.org).

The upstream project is tracked as a submodule in this repo.

## clone
```shell
$ git clone https://github.com/intel-media-ci/cartwheel-gst-plugins-bad --recursive
```

## apply patches
```shell
# at top-level directory
$ git submodule update --init --recursive
# at submodule directory
$ cd gst-plugins-bad
# It is recommended to create a branch before applying the patches
$ git checkout -b <my new branch>
$ git am ../patches/*.patch
```

## rebase
```shell
# at top-level directory
$ git pull --rebase --recurse-submodule
```

## administrators

To update the submodule reference commit id to the latest upstream:

```shell
# at top-level directory
$ git submodule update --remote --recursive
$ git commit -sam "$(git diff --submodule | head -1 | sed 's/:$//')"
```

...verify the patches still apply successfully.  If they don't apply, fix them and include in new commit(s).

## additional information

For more information and examples about Git Submodules, see https://git-scm.com/book/en/v2/Git-Tools-Submodules
