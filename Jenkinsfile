pipeline {
  agent any
  stages {
    stage('Source') {
      steps {
        git(url: 'https://github.com/bokdoll/blue-green-deployment-test.git', branch: 'master', poll: true, credentialsId: 'bokdoll')
      }
    }

    stage('Build') {
      steps {
        sh 'npm build'
      }
    }

    stage('Deploy') {
      steps {
        sh 'echo "Deploy Success"'
      }
    }

  }
}