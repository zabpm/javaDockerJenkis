pipeline {
    agent {
        docker {
            image 'maven:3.3.9-adoptopenjdk-11'
            args '-v /root/.m2:/root/.m2'
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