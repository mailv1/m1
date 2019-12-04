pipeline {
  agent any


job('m1') {
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
}
