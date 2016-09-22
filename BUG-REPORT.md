There seems to a [bug](https://issues.jenkins-ci.org/browse/JENKINS-38406) in the git-plugin where in, if a build
parameter is part of branch spec, the jenkins job checks out a wrong branch.

Detailed info on the bug in the [jira ticket](https://issues.jenkins-ci.org/browse/JENKINS-38406). I reproduced the bug
from an out-of-the-box jenkins created from this repo. I have the docker image pushed at puneethn/jenkins-git-bug:latest.

````
docker run -i --rm -p 8080:8080 -p 50000:50000 -t puneethn/jenkins-git-bug:latest
````

````
username: admin
password: password
````

Refer to the build parameter `sha1` and branch built for jobs 8 and 9.
