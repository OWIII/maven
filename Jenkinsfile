pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
          sh 'mvn clean compile'
      }
      post {
        success {
          echo 'Archiving...'
          achiveArtifacts artifacts: '**/target/*.war'
        }
      }
    }
    stage ('Deploy') {
      steps {
        echo "Deploy step..."
      }
    }
  }
}
