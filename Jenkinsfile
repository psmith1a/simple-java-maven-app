pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2 --network=host'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh 'echo \'Hi from new pipeline\''
            sh 'echo \'Hi from test\''
            sh 'echo \'hi again\''
          }
        }
        stage('Parallel step') {
          steps {
            echo 'Hi parallel'
          }
        }
      }
    }
  }
}