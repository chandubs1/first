pipeline {
  agent {
    docker {
      image 'maven:3.3.9-jdk-8'
      args '-e "http_proxy=http://www-proxy.us.oracle.com:80" -e "https_proxy=https://www-proxy.us.oracle.com:80"  -d -ti -v  /home/chbs/.m2:/root/.m2 --privileged'
    }

  }
  stages {
    stage('Init') {
      steps {
        echo 'Hello from Blue Ocean Chandu'
      }
    }
  }
  tools {
    maven 'M3'
    jdk 'jdk8'
  }
}