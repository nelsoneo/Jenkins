pipeline {
  agent any
  stages {
    stage('Update') {
      parallel {
        stage('Update') {
          steps {
            build 'Update'
            catchError(buildResult: 'failure') {
              build(job: 'build', quietPeriod: 5)
            }

          }
        }

        stage('KB-Nucleo') {
          steps {
            echo 'pronto'
          }
        }

        stage('KB-NFSe') {
          steps {
            echo 'pronto'
          }
        }

        stage('Nfe-NFCe') {
          steps {
            echo 'pronto'
          }
        }

        stage('MDFe') {
          steps {
            echo 'pronto'
          }
        }

        stage('CTe') {
          steps {
            echo 'pronto'
          }
        }

      }
    }

  }
}