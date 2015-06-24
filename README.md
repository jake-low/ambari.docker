# ambari.docker

Build the image you want:

```
cd <version>
docker build -t ambari:<version> .
```

Then run it:

```
docker run -it -p 8080:8080 -p 8440:8440 -p 8441:8441 ambari:<version> ambari-server start
```

Now connect to `localhost:8080`. You should see a webui. You can now use your local machine as an ambari server.
