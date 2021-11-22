pipeline {
  agent any

  stages {
    stage('Checkout') {
    steps {
	    git branch: 'master', credentialsId: 'xxxx', url: 'git@github.com:nimishajn/multi-tier-application.git'
	}
	}

    stage('Provisioner Multi-web application') {
      parallel {
        stage('docker-compose up') {
          steps {
            sh 'docker-compose up'
          }
        }
        
      }
    }
  }
}

