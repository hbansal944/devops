pipeline {
  agent any
  tools {
    maven 'maven1'
  }
  stages {
    stage('Checkout Stage') { // Capitalized names for better readability
      steps {
        checkout scmGit(
          branches: [[name: '*/main']],
          extensions: [],
          userRemoteConfigs: [[url: 'https://github.com/hbansal944/devops.git']]
        )
      }
    }
    stage('Build Maven Stage') { // Capitalized names for better readability
      steps {
        sh 'mvn clean install' // Use 'sh' for shell commands on Unix-like systems
      }
    }
  }
}
