Create a Rails app :
```no-highlight
docker run --rm -ti -v `pwd`:/app clmntlxndr/rails new APP_NAME .
```

Run a Rails app :
```no-highlight
docker run --rm -ti -v `pwd`:/app clmntlxndr/rails s
```

Bundle ?
```no-highlight
docker run --rm -ti -v --entrypoint=bundle `pwd`:/app clmntlxndr/rails install
```
