pipeline {
  agent any

  parameters {
    string(name: 'ENVIRONMENT', defaultValue: 'dev', description: 'Select environment')
    booleanParam(name: 'DEPLOY', defaultValue: true, description: 'Deploy after build?')
  }

  stages {
    stage('Checkout') { steps { checkout scm } }

    stage('Build') {
      steps {
        echo "Building for environment: ${params.ENVIRONMENT}"
        sh 'echo Build OK'
      }
    }

    stage('Deploy') {
      when { expression { params.DEPLOY } }
      steps { sh 'echo Deploying…' }
    }
  }
}
