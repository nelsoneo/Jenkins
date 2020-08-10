pipeline {
  agent any
  stages {
    stage('Update') {
      steps {
        build 'Update'
        catchError(buildResult: 'failure') {
          build 'build'
        }

      }
    }

  }
}