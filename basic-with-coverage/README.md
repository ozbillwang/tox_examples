# Usage

### Clone the source code
```
git clone git@github.com:bmaddali/python_tox_basic.git
cd python_tox_basic/basic
```

### Start sonarqube container
```
docker run -d --name sonarqube -p 9000:9000 -p 9092:9092 sonarqube
```

### Get your computer’s IP address

```
ifconfig |grep 192 
	inet 192.168.1.107 netmask 0xffffff00 broadcast 192.168.1.255
```

### Run test and coverage 
```
tox
```
you should see coverage.xml in the root directory


### Run sonarqube scanner

Update IP address in file `sonar-project.properties`
```
docker run --rm -v $(pwd):/usr/src sonarsource/sonar-scanner-cli
```
you should see coverage metrics in sonarqube now.
