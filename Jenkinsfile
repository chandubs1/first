pipeline {
  agent {
    docker {
      image 'maven:3.3.9-jdk-8'
      args '-e "http_proxy=http://www-proxy.us.oracle.com:80" -e "https_proxy=https://www-proxy.us.oracle.com:80"  -d -ti --name VM1'
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
  environment {
    ENV = 'https_proxy="https://www-proxy.us.oracle.com:80"'
  }
}