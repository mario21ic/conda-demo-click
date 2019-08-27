# conda-demo-click

Requirements:
```
$ conda install -y conda-build
$ conda install -y anaconda-client
```

Upload to anaconda.org automatically
```
$ conda config --set anaconda_upload yes
```

Generate with label cuda10
```
$ conda build --label cuda10 --label auto --python=3.7 --output-folder $PWD/py37_cuda10/ .
```

Generate with another label
```
$ conda build --label cuda92 --label auto --python=3.7 --output-folder $PWD/py37_cuda92/ .
```
