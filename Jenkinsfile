pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
          bat 'mvn clean compile'
      }
      post {
        success {
          echo 'Archiving...'
          archiveArtifacts artifacts: '**/target/*.war'
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
