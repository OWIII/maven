pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        sh 'mvn clean package'
      }
      post {
        success {
          echo 'Archiving...'
          achiveArtifacts artifacts: '**/target/*.war'
        }
      }
    }
    stage ('Build') {
      steps {
        echo "Build step..."
      }
    }
    stage ('Deploy') {
      steps {
        echo "Deploy step..."
      }
    }
  }
}
