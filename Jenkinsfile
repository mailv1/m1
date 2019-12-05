pipeline {
  agent any

  options {
    // Only keep the 10 most recent builds
    //buildDiscarder(logRotator(numToKeepStr:'10'))
   // echo "In Options"
   disableConcurrentBuilds()  
  }
  stages {
    stage ('Install') {
      steps {
        // install required bundles
        //sh 'bundle install'
        echo "In Install"
        sh "sleep 420"
      }
    }
  }


  post {
    always {
      echo "Send notifications for result: ${currentBuild.result}"
    }
  }
}
