pipeline {
  agent any
  stages {
    stage('Update') {
      parallel {
        stage('Update') {
          steps {
            echo 'update kb'
            build(job: 'update', propagate: true)
          }
        }

        stage('Passo1') {
          steps {
            build(job: 'paso1', propagate: true)
          }
        }

      }
    }

  }
  triggers {
    cron('H/3 * * * *')
  }
}