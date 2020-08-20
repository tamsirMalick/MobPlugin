pipeline {
  agent any
  tools {
    gradle 'gradle66'
  }
  stages {
    stage('build') {
      steps {
          bat 'gradlew assembleDebug'
        }
    }

    stage('mobsf scan') {
      steps {
        bat 'gradlew scan'
      }
    }

    stage('mobsf check status') {
      steps {
        bat 'gradlew checkStatus'
      }
    }

    stage('mobsf getReport') {
      steps {
        bat 'gradlew getReport'
      }
    }
}
