pipeline  {
     agent {label 'master'}
    stages {
     stage('build') {
       steps {
       sh 'ant -f build.xml -v'
       }
      }
     }
  post {
   always {
    archiveartifacts artifacts: 'dist/*.jar', fingerprint: true
     }
    }
  }
