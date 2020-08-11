pipeline {
  agent any
     triggers {
        cron('H/3 * * * *')
    }
  stages {
    stage('Update') {
      parallel {
        stage('Update') {
          steps {
            echo 'pronto'
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
}
