pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 1, units: 'MINUTES')
        disableconcurrentbuilds()
    }
    stages {
        stage('Build') {
            steps {
               sh 'echo This is build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo This is deploy'
            }
        }
    }
}