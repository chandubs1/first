pipeline {
  agent any
  stages {
    stage('Initialize') {
      parallel {
        stage('Initialize') {
          steps {
            sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            echo 'Hello chandu'
          }
        }
        stage('echo') {
          steps {
            sh '''echo Chandu from Blue Ocean
'''
          }
        }
      }
    }
    stage('Build') {
      steps {
        sh 'echo "Hello World"'
        sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
      }
    }
  }
  tools {
    maven 'M3'
    jdk 'jdk8'
  }
}