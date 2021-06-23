# conda-demo-click

Requirements:
```
$ conda create python=3.8 -n bld1 -y
$ conda activate bld1
$ conda install -y conda-build anaconda-client
```

Building:
```
conda build --dirty --label auto --python=3.8 --output-folder $PWD/build/ ./
```

Generate with label cuda10
```
$ conda build --label cuda10 --label auto --python=3.7 --output-folder $PWD/py37_cuda10/ ./
```

Generate with another label
```
$ conda build --label cuda92 --label auto --python=3.7 --output-folder $PWD/py37_cuda92/ ./
```

Installing:
```
$ conda install build/linux-64/click-7.0-py38_0.tar.bz2
```

Uploading
```
$ anaconda -t $TOKEN upload -u mario21ic-nightly --force py37_cuda10/linux-64/click-7.0-py37_0.tar.bz2
```

(Optional) upload to anaconda.org automatically
```
$ conda config --set anaconda_upload yes
```
