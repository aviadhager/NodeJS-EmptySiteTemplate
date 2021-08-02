pipeline {
  agent {
    node {
      label 'centof7'
    }

  }
  stages {
    stage('Check out from github') {
      steps {
        git(url: 'https://github.com/aviadhager/NodeJS-EmptySiteTemplate.git', branch: 'master', credentialsId: 'github')
      }
    }

  }
}