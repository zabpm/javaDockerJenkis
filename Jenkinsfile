pipeline {
    agent {
        docker {
            image 'maven:3.8-adoptopenjdk-8'
            args '-v ~/.m2:/var/maven/.m2'
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