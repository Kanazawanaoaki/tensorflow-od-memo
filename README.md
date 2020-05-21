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
```

```
pip install Cython
pip install contextlib2
pip install pillow
pip install lxml
pip install jupyter
pip install matplotlib
```

clone repository
```
git clone https://github.com/tensorflow/models.git
```
path set
```
# From tensorflow/models/research/
export PYTHONPATH=$PYTHONPATH:`pwd`:`pwd`/slim
```

env test
```
# in Ubuntu
# protoc -I=./ --python_out=./ ./object_detection/protos/*.proto

# From tensorflow/models/research/
python object_detection/builders/model_builder_tf1_test.py
```

## test sample

```
jupyter-notebook object_detection/object_detection_tutorial.ipynb 
```
