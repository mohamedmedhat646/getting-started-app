pipeline {
  agent any
  stages {
    stage('Checkout') { steps { checkout scm } }   // Jenkins أصلاً هيعمل checkout لو job من SCM
    stage('Build')    { steps { sh 'echo Build OK' } }
  }
}
