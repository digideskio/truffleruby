# Docker Test Images

These are Dockerfiles to test TruffleRuby builds on different Linux
distributions. They could also serve as sources on which to base a deployment
image, but we'd recommend the official GraalVM Dockerfile for that.

https://github.com/oracle/docker-images/tree/master/GraalVM

These Dockerfiles run the tests as part of the image build, so if the image
successfully builds then the tests have all passed.

You need to put the built GraalVM binary tarball into the same directory as the
Dockerfile, and update the Dockerfile for the version.

```
$ docker build -t truffleruby-test-ubuntu .
```

Docker will need to run the container with at least 8 GB of RAM if you are using
virtualisation, to give enough space for the AOT image to build.
