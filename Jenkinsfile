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

            mail(subject: 'Error de update', body: 'teste', to: 'nelsoneo@gmail.com')
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