pipeline {
  agent any
  stages {
    stage('Update') {
      steps {
        echo 'update kb'
        build(job: 'update', propagate: true)
        catchError(buildResult: 'FAILURE', stageResult: 'FAILURE', message: 'falho o update')
      }
    }

  }
}
