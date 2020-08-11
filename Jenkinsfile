pipeline {
  agent any
  stages {
    stage('Update') {
      steps {
        echo 'update kb'
        build(job: 'update', propagate: true)
      }
    }

  }
}