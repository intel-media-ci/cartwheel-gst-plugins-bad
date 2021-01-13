# cartwheel : gst-plugins-bad

## apply patches
```shell
$ git submodule update --init --recursive
$ cd gst-plugins-bad
# It is recommended to create a branch before applying the patches
$ git checkout -b <my new branch>
$ git am ../patches/*.patch
```
