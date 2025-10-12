pipeline {
    agent any
    parameters {
        string(name: 'ENVIRONMENT', defaultValue: 'dev', description: 'Select environment')
        booleanParam(name: 'DEPLOY', defaultValue: true, description: 'Deploy after build?')
    }
    stages {
        stage('Build') {
            steps {
                echo "Building for environment: ${params.ENVIRONMENT}"
            }
        }
    }
}

pipeline {
  agent any
  stages {
    stage('Checkout') { steps { checkout scm } }   // Jenkins أصلاً هيعمل checkout لو job من SCM
    stage('Build')    { steps { sh 'echo Build OK' } }
  }
}
