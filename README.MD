# React Native Docker
React Native Docker is a docker image that helps you to compile and run your react native project in any environment.
  - Helps you to build easily
  - Updated regularly
  - Published on Docker Hub
  
### Docker Installation

Download annd install Docker in your machine. 
[Docker Mac OS](https://docs.docker.com/docker-for-mac/install/) | [Docker Windows](https://docs.docker.com/docker-for-windows/install/)

### Usage

Installation successful? Great!
Now lets download the image and run

Open your favorite Terminal and run these commands.


Step 1:
```sh
$ git clone git@github.com:imjaahh/react-native-docker.git
```
Step 2:
```sh
$ cd react-native-docker
$ docker build ./
```
Step 3 (optional):
Accept all licenses, it might cause some build issue while the gradle dependencies are being downloaded
```sh
$  yes | $ANDROID_HOME/tools/bin/sdkmanager "build-tools;24.0.3"
```
Step 4:
```sh
$ cd [your react native project]
```
Step 5:
```sh
$ docker run --rm -ti -v `pwd`:/app imjaahh/react-native-docker bash
```
Step 6:
```sh
$ cd app
```
Step 7:
```sh
$ cd android && ./gradlew assembleRelease
```
