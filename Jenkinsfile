pipeline {
    agent {
        docker {
            image 'maven:3.8-adoptopenjdk-8'
            args '-v C:/apache-maven-3.3.9-bin:C:/apache-maven-3.3.9-bin'
        }
	}
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('QA') {
            steps {
                echo 'QA'
            }
        }
    }
}