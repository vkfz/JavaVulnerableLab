pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile'
    }

  }
  stages {
    stage('Compile Stage') {
      steps {
        withMaven(maven: 'Maven_home') {
          sh 'mvn clean compile'
        }

      }
    }
    stage('Package Stage') {
      steps {
        withMaven(maven: 'Maven_home') {
          sh 'mvn package'
        }

      }
    }
  }
}