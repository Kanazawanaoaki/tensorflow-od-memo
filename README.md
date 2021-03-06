# tensorflow-memo
Tensorflowのテストをする。　　

## set env

```
mkdir tf_dir
cd tf_dir
virtualenv tf_env
source tf_env/bin/activate
```

install with https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/installation.md
```
pip install tensorflow==1.15
# actually tensorflow 2.x ?
# pip install -U --pre tensorflow=="2.*"
```

```
pip install Cython
pip install contextlib2
pip install pillow
pip install lxml
pip install jupyter
pip install matplotlib

# in Ubuntu
# pip install pathlib
```

clone repository
```
git clone https://github.com/tensorflow/models.git
```
path set
```
# in Ubuntu
# protoc -I=./ --python_out=./ ./object_detection/protos/*.proto

# From tensorflow/models/research/
export PYTHONPATH=$PYTHONPATH:`pwd`:`pwd`/slim
```

env test
```
# From tensorflow/models/research/
python object_detection/builders/model_builder_tf1_test.py
```

## test sample

```
jupyter-notebook object_detection/object_detection_tutorial.ipynb
```
