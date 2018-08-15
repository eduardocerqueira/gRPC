gRPC
====

this repo is for personal use and for learning purpose only.

- https://grpc.io/docs/guides/
- https://grpc.io/docs/quickstart/python.html#prerequisites

requires
```
sudo dnf install pipenv
```

Setup env

```
$ pipenv --python 3
$ pipenv install --dev
$ pipenv shell
```


SERVER


CLIENT




ISSUES

1. Running setup.py install for googleapis-common-protos ... error
 AttributeError: '_NamespacePath' object has no attribute 'sort'. Fix upgrading your system:
    ```
    pip install --upgrade pip
    pip install --upgrade setuptools
    pip install -r requirements.txt
    ```

1.

