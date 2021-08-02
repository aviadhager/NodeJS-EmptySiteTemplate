pipeline {
  agent {
    node {
      label 'centof7'
    }

  }
  stages {
    stage('error') {
      steps {
        git(url: 'https://github.com/aviadhager/NodeJS-EmptySiteTemplate.git', credentialsId: 'github', branch: 'master')
      }
    }

  }
}