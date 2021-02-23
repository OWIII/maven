pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        withMaven(maven : 'apache-maven-3.6.3') {
          bat'mvn clean compile'
        }
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
