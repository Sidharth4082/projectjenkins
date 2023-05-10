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
        stage('Deploy to Tomcat') {
            steps {
                sh 'curl -T C:\Jenkins\workspace\maven-project\target http://localhost:8081/manager/text/deploy?path=/my-project-1.0.0&update=true -u deployer:deployer'
            }
        }
        
    }
}