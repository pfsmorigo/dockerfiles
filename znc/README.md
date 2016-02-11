### Configuration

```
mkdir -p <data-dir>
docker run --rm -it -v <data-dir>:/var/lib/znc pfsmorigo/znc --makeconf
```

### Running

```
docker run -d -p 16667:16667 -v <data-dir>:/var/lib/znc --name znc pfsmorigo/znc
```

Go to http://IP:16667 in a web browser, and voila!


Based on https://github.com/voxxit/dockerfiles/tree/master/znc
