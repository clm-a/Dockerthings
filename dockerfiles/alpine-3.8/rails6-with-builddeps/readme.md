Creates Rails 6 app keeping builddeps in Apline
Build runtime and docker-compose image with appropriate Dockerfile (not this one)

```sh
docker run --rm -v `pwd`:/app -w /app clmntlxndr/rails6-with-builddeps rails new my_app # creates app in current dir
cd my_app && docker run --rm -ti -v `pwd`:/app -w /app clmntlxndr/rails6-with-builddeps sh # have a look into your app
```
