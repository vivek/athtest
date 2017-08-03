pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    stage('Browser Tests') {
      steps {
        parallel(
          "Firefox": {
            sh 'echo \'setting up selenium environment\''
            
          },
          "Safari": {
            sh 'echo \'setting up selenium environment\''
            
          },
          "Chrome": {
            sh 'echo \'setting up selenium environment\''
            sh 'ping -c 3 localhost'
            
          },
          "Internet Explorer": {
            sh 'echo \'setting up selenium environment\''
            sh 'ping -c 4 localhost'
            
          }
        )
      }
    }
    stage('Static Analysis') {
      steps {
        echo 'Static analysis...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying now...'
      }
    }
  }
  post {
    always {
      echo 'archving test results'
      
    }
    
  }
}
