pipeline {
    agent any
  
  	tools { 
        maven 'maven-3.8.1'
        jdk 'jdk8' 
    }

    stages {
        stage('Build') {
            steps {
                // To run Maven on a Windows agent, use
                 bat 'mvn clean test'
            }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    //junit '**/target/surefire-reports/TEST-*.xml'
                    //archiveArtifacts 'target/*.jar'
					echo 'success'
                }
            }
        }
    }
}
