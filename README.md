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

issues

1. Running setup.py install for googleapis-common-protos ... error
 AttributeError: '_NamespacePath' object has no attribute 'sort'. Fix upgrading your system:
    ```
    pip install --upgrade pip
    pip install --upgrade setuptools
    pip install -r requirements.txt
    ```

Summary
-------

**gRPC**

* defining a service
* specifying the methods that can be called remotely with their parameters and return types. 

On the server side: 

* the server implements this interface and runs a gRPC server to handle client calls. 

On the client side:

* the client has a stub (referred to as just a client in some languages) that provides the same methods as the server.

**Protocol Buffer**

Google’s open source mechanism for serializing structured data

* in .proto file define structure for data you want to serialize, e.g:

```
message System {
  string name = 1;
  int32 id = 2;
  bool is_enabled = 3;
}
```

* use protocol buffer compiler protoc to generate data access classes in your preferred language(s) from your proto definition, e.g:

```
from grpc_tools import protoc

protoc.main((
    '',
    '-I../protos',
    '--python_out=.',
    '--grpc_python_out=.',
    '../protos/helloworld.proto',
))
```

ref
---

-- Talks and presentations
* https://grpc.io/docs/talks/
* https://www.infoq.com/presentations/grpc
* https://blog.openshift.com/openshift-commons-briefing-69-grpc-microservices-openshift-ray-tsang-google/

-- sites and blogs
* https://medium.com/@sankar.p/how-grpc-convinced-me-to-chose-it-over-rest-30408bf42794
* https://opensource.google.com/projects/grpc
* https://grpc.io/
* https://developers.google.com/protocol-buffers/docs/overview




