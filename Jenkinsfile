pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 1, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
        stage("print params") {
            steps{
                echo "Hello ${params.PERSON}"
                echo "biography ${params.BIOGRAPHY}"
                echo "toggle ${params.TOGGLE}"
                echo "choice ${params.CHOCIE}"
                echo "password ${params.PASSWORD}"
            }
        }
    }
}