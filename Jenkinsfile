pipeline {
  agent any
  stages {
    stage('Check out from github') {
      steps {
        git(url: 'https://github.com/aviadhager/NodeJS-EmptySiteTemplate.git', branch: 'master', credentialsId: 'github')
      }
    }

    stage('install depend') {
      steps {
        sh 'npm install'
      }
    }

    stage('running the app') {
      steps {
        sh 'npm start &'
      }
    }

    stage('test the app') {
      steps {
        sh 'curl localhost:8080'
      }
    }

    stage('kill app') {
      steps {
        sh 'pkill -f node'
      }
    }

    stage('archive and clean') {
      steps {
        sh 'zip -r package.zip .'
        archiveArtifacts(artifacts: 'package.zip', onlyIfSuccessful: true)
        cleanWs(cleanWhenSuccess: true)
      }
    }

  }
}