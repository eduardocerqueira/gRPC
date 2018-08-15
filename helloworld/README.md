after changes to helloworld.proto 

```
pipenv shell
cd helloworld
python run_codegen.py
```

Start server

```
pipenv shell
cd helloworld 
python greeter_server.py
```

Run tests

```
pipenv shell
cd helloworld 
pytest -v -s test_greeter_server.py
```
