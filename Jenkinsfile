pipeline {
  agent any
  stages {
    stage('build') {
      agent any
      steps {
        withGradle() {
          sh './gradlew \'assembleDebug\''
        }

      }
    }

    stage('mobsf scan') {
      steps {
        sh './gradlew \'scan\''
      }
    }

    stage('mobsf check status') {
      steps {
        sh './gradlew \'checkStatus\''
      }
    }

    stage('mobsf getReport') {
      steps {
        sh './gradlew \'getReport\''
      }
    }

  }
}