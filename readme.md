docker run -p8080:8080 -v /home/garrin/Code/jenkins/jenkins_home:/var/jenkins_home helvegr/jenkins


curl -s -k "http://admin:admin@localhost:8080/pluginManager/api/json?depth=1" | jq -r '.plugins[].shortName' | tee plugins.txt