pipeline {
  agent any
  tools {
    maven 'maven1'
  }
  stages {
    stage('Checkout') { 
      steps {
        checkout scmGit(
          branches: [[name: '*/main']],
          extensions: [],
          userRemoteConfigs: [[url: 'https://github.com/hbansal944/devops.git']]
        )
      }
    }
    stage('Maven Build') {
      steps {
        bat 'mvn clean install' 
      }
    }
    stage('Maven Test') {
      steps {
        bat 'mvn test'
      }
    }
  }
}
