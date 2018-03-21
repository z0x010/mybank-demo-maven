pipeline {
  agent none
  stages {
    stage('build') {
      steps {
        sh 'jar cvf aa.war *'
        echo 'build war'
      }
    }
    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test'
          }
        }
        stage('sec test') {
          steps {
            echo 'sec test'
            sleep 11111
          }
        }
      }
    }
  }
}