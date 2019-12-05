//Execute concurrent builds if necessary
pipeline {
  agent any


  stages {

    stage('stage1') {
      blockOn([m1]) {
        blockLevel('GLOBAL')
        scanQueueFor('ALL')
      steps {
            sh 'sleep 420 '
	}
      } 
  }

 }

}
