pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building the resource from github repository'
          }
        }

        stage('Build docker image') {
          steps {
            sh 'sudo docker-compose up -d'
          }
        }

        stage('List docker image') {
          steps {
            sh 'docker images'
          }
        }

      }
    }

  }
}