pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building the resource from github...'
        git(changelog: true, credentialsId: 'github-credential', poll: true, url: 'https://github.com/PHO-KHAING/ci_admin.git', branch: 'main')
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker-compose up -d'
      }
    }

  }
}