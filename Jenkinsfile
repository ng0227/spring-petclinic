pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh './mvnw package'
      }
    }

    stage('Sonar Qube') {
      steps {
        sh '''./mvnw sonar:sonar -Dsonar.projectKey=petclinic_static_analysis ./mvnw sonar:sonar -Dsonar.projectKey=afa572edc406cad06b0a741d6283fb6b1df6467f
'''
      }
    }

  }
}