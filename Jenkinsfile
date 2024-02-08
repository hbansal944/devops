pipeline {
  agent any
  tools {
    maven 'maven1'
  }
  stages {
    stage('Checkout Stage') { 
      steps {
        checkout scmGit(
          branches: [[name: '*/main']],
          extensions: [],
          userRemoteConfigs: [[url: 'https://github.com/hbansal944/devops.git']]
        )
      }
    }
    stage('Build Maven Stage') {
      steps {
        bat 'mvn clean install' 
      }
    }
  }
}
