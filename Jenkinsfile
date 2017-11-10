pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                checkout scm
                sh 'sbt clean compile test'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}