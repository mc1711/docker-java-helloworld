# docker-java-helloworld
execute a basic java in docker container

## Build a docker image from java class
$docker build --tag "docker-hello-world:latest" .

Sending build context to Docker daemon  61.44kB
Step 1/4 : FROM alpine:latest
 ---> 3f53bb00af94
Step 2/4 : ADD HelloWorld.class HelloWorld.class
 ---> 67709d08a9b3
Step 3/4 : RUN apk --update add openjdk8-jre
 ---> Running in 0bb2b087d609
fetch http://dl-cdn.alpinelinux.org/alpine/v3.8/main/x86_64/APKINDEX.tar.gz
fetch http://dl-cdn.alpinelinux.org/alpine/v3.8/community/x86_64/APKINDEX.tar.gz
(1/39) Installing libffi (3.2.1-r4)
(2/39) Installing p11-kit (0.23.10-r0)
(3/39) Installing libtasn1 (4.13-r0)
(4/39) Installing p11-kit-trust (0.23.10-r0)
(5/39) Installing ca-certificates (20190108-r0)
(6/39) Installing java-cacerts (1.0-r0)
(7/39) Installing libgcc (6.4.0-r9)
(8/39) Installing nspr (4.19-r0)
(9/39) Installing sqlite-libs (3.25.3-r0)
(10/39) Installing libstdc++ (6.4.0-r9)
(11/39) Installing nss (3.36.1-r1)
(12/39) Installing libxau (1.0.8-r2)
(13/39) Installing libbsd (0.8.6-r2)
(14/39) Installing libxdmcp (1.1.2-r4)
(15/39) Installing libxcb (1.13-r2)
(16/39) Installing libx11 (1.6.6-r0)
(17/39) Installing libxcomposite (0.4.4-r1)
(18/39) Installing libxext (1.3.3-r2)
(19/39) Installing libxi (1.7.9-r1)
(20/39) Installing libxrender (0.9.10-r2)
(21/39) Installing libxtst (1.2.3-r1)
(22/39) Installing alsa-lib (1.1.6-r0)
(23/39) Installing libbz2 (1.0.6-r6)
(24/39) Installing libpng (1.6.37-r0)
(25/39) Installing freetype (2.9.1-r1)
(26/39) Installing giflib (5.1.4-r2)
(27/39) Installing libjpeg-turbo (1.5.3-r4)
(28/39) Installing openjdk8-jre-lib (8.212.04-r0)
(29/39) Installing java-common (0.1-r0)
(30/39) Installing krb5-conf (1.0-r1)
(31/39) Installing libcom_err (1.44.2-r0)
(32/39) Installing keyutils-libs (1.5.10-r0)
(33/39) Installing libverto (0.3.0-r1)
(34/39) Installing krb5-libs (1.15.4-r0)
(35/39) Installing lcms2 (2.9-r1)
(36/39) Installing pcsc-lite-libs (1.8.23-r1)
(37/39) Installing lksctp-tools (1.0.17-r0)
(38/39) Installing openjdk8-jre-base (8.212.04-r0)
(39/39) Installing openjdk8-jre (8.212.04-r0)
Executing busybox-1.28.4-r2.trigger
Executing ca-certificates-20190108-r0.trigger
Executing java-common-0.1-r0.trigger
OK: 82 MiB in 52 packages
Removing intermediate container 0bb2b087d609
 ---> bd133c72ff0f
Step 4/4 : ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "HelloWorld"]
 ---> Running in 6d63cc3d6692
Removing intermediate container 6d63cc3d6692
 ---> d2d56253f788
Successfully built d2d56253f788
Successfully tagged docker-hello-world:latest


## Create and Run a container from the image
$docker run docker-hello-world:latest
Helloo World !!