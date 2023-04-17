pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test"
            }
        }
        stage('--package--') {
            agent {label 'ec2_slave1'}
            steps {
                sh "mvn package"
            }
        }
    }
}
