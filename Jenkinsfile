pipeline {
    agent any
    stages {
      stage('Build') {
          steps {
               echo "Build"
          }
        }
      stage('test') {
          steps {
               echo "test"
            }
        }
      stage('Integration Test') {
          steps {
               echo "Build"
            }
        }
    }
    
    post {
        always {
            echo "Hi there"
        }
        success {
            echo "job ran successfully"
        }
        failure {
            echo "job ran successfully. Please try again"
        }
    }

}
