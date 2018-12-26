<<<<<<< HEAD
pipeline {
          agent any
           stages {
           stage('unit Tests'){
           steps {
           sh 'ant -f test.xml -v'
            junit 'reports/result.xml'
                 }
                              }
            stage('build') {
             steps {
              sh "ant -f build.xml -v"
  }
 }
           stage('deployment') {
            steps {
      sh "cp dist/rectangle_${env.BUILD_NUMBER}.jar /var/www/html/rectangles/all/"
                    }
                                }
}
post {
 always {
  archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
    }
   }
}

=======
pipeline  {
     agent {label 'master'}
    stages {
    stage('unit Tests') {
      steps {
        sh 'ant -f test.xml -v'
        junit 'reports/result.xml'
       }
     }
     stage('build') {
       steps {
       sh 'ant -f build.xml -v'
       }
      }
     }
  post {
   always {
    archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
     }
    }
  }
>>>>>>> 00c910cc90d36239098e92141f4139bbb8982e7c
