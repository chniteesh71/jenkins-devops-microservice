node {
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
        stage('Integration Test') {
                echo "Test"
        }

}
# or 
node {
                echo "Build"
                echo "Test"
                echo "Test"

}

# we can run using above code also without stages using scripted pipeline but with declarative have to use
# stages,steps
# Scripted pipeline is above one.
# declarative pipeline 
pipeline {
    agent any
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
