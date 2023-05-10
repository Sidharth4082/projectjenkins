pipeline {
    agent any
    tools {
	  maven 'Minstall'      
	}
    stages {

        stage('Build') {

            steps {
                sh 'mvn clean package'
            }
        }
        stage("Test") {
            steps {
                sh 'mvn test'
            }
        }
    }
}