### Configuration

```
mkdir -p <data-dir>
docker run --rm -it -v <data-dir>:/var/lib/znc pfsmorigo/znc --makeconf
```

### Running

```
docker run -d -p <extport>:7000 -v <data-dir>:/var/lib/znc --name znc pfsmorigo/znc
```

### Debug
```
docker run -t -p <extport>:7000 -v <data-dir>:/var/lib/znc --name znc --entrypoint /bin/bash pfsmorigo/znc

```

Go to http://IP:16667 in a web browser, and voila!


Based on https://github.com/voxxit/dockerfiles/tree/master/znc

