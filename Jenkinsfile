//Execute concurrent builds if necessary
pipeline {
  agent any


  stages {

  blockOn([m1]) {
        blockLevel('GLOBAL')
        scanQueueFor('ALL')
    stage('stage1') {
      steps {
        sh 'sleep 420 '
        }
      }

      } 

    }

}

