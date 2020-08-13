pipeline {
  agent any
  stages {
    stage('Update') {
      parallel {
        stage('Update') {
          steps {
            echo 'update kb'
          }
        }

        stage('kb-park') {
          steps {
            build(job: 'update', propagate: true)
          }
        }

        stage('kb-farmacia') {
          steps {
            echo 'pronto'
          }
        }

      }
      post {
        failure {
          stage: 'IHML'
        }
      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'pronto build'
          }
        }

        stage('kb-park') {
          steps {
            echo 'pronto'
          }
        }

      }
    }

    stage('IHML') {
      steps {
        echo 'pronto ihml'
      }
    }

    stage('Test') {
      steps {
        echo 'pronto test'
      }
    }

    stage('Compilation') {
      steps {
        echo 'pronto compilation'
      }
    }

  }
}
