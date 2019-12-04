pipeline {
  agent any



    blockOn([m1]) {
        blockLevel('GLOBAL')
        scanQueueFor('ALL')

  stages {
    stage('stage1') {
      steps {
        sh 'sleep 420 '
        }
      }

    }

  }


}

