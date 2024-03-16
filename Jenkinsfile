pipeline {
    // agent any
    agent { docker { image 'maven:3.6.3'} }
    stages {
      stage('Build') {
          steps {
               sh 'mvn --version'
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
         /*unstable {
            echo "Incase of test failure. This will execute"
        }
         changed {
            echo "Incase of status of build change. This will execute"
        }*/
        
    }

}
