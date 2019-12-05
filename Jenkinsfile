pipeline {
  agent any

 // options {
    // Only keep the 10 most recent builds
    //buildDiscarder(logRotator(numToKeepStr:'10'))
   // echo "In Options"
 // }
  stages {
    stage ('Install') {
      steps {
        // install required bundles
        //sh 'bundle install'
        echo "In Install"
      }
    }
  }


  post {
    always {
      echo "Send notifications for result: ${currentBuild.result}"
    }
  }
}
