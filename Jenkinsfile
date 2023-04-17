pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "/opt/maven/bin/mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "/opt/maven/bin/mvn test"
            }
        }
        stage('--package--') {
            agent {label 'ec2_slave1'}
            steps {
                 sh "/opt/maven/bin/mvn package"
            }
        }
    }
}
