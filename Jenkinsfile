pipeline {
  agent {
    docker {
      image 'ubuntu'
      args '-u root -e "http_proxy=http://www-proxy.us.oracle.com:80" -e "https_proxy=https://www-proxy.us.oracle.com:80"  -d -ti '
    }

  }
  stages {
    stage('Init') {
      steps {
        echo 'Hello from Blue Ocean Chandu'
      }
    }
    stage('error') {
      steps {
        sh '''apt-get -y update
apt-get install -y python python-pip wget'''
      }
    }
  }
  tools {
    maven 'M3'
    jdk 'jdk8'
  }
}