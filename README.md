# jenkins-buildpack
Cloud Foundry Jenkins Buildpack

### How to use

To run app with this buildpack you need do the following: 

```
cf push jenkins-app-name -p jenkins.war -m 4G -b https://github.com/kenanhancer/jenkins-buildpack.git
```

Here are descriptions of each parameter:

* `jenkins-app-name` is the name of application inside of Cloud Foundry.
* `-p <path>` shows Cloud Foundry CLI where to take sources or binaries to run the app.
* `-m <memory-quota>` stands for memory limit for the app, jenkins 2.0 with java 8 seems to require somrthing like 4Gb of memory for 
* `-b <buildpack>` sets what buildpack should be used to run this app; if you specify repo URL, CF will fetch it.