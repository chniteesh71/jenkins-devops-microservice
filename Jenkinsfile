pipeline {
  //agent { docker { image 'node'} } 
  agent any
  environment {
    dockerHome = tool 'myDocker'
    mavenHome = tool 'myMaven'
    PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
  }
  stages {
    stage('Build') {
      steps {
            sh 'docker --version'
            sh 'mvn --version'
            echo "Build"
            echo "$PATH"
            echo "BUILD_NUMBER - $env.BUILD_NUMBER"
            echo "BUILD_ID - $env.BUILD_ID"
            echo "JOB_NAME - $env.JOB_NAME"
            echo "BUILD_TAG - $env.BUILD_TAG"
            echo "BUILD_URL - $env.BUILD_URL"
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
        /*failure {
            echo "job failed. Please try again"
        }
          unstable {
            echo "Incase of test failure. This will execute"
        }
         changed {
            echo "Incase of status of build change. This will execute"
        }*/
  }

}
