pipeline {

    agent any

    triggers {
        pollSCM '*/1 * * * *'
    }

    stages {

        stage('Compile') {
            steps {
                sh 'echo Compiling...'
            }
        }

        stage('Test') {
            steps {
                sh 'echo Testing...'
            }
        }

        stage('Package') {
            steps {
                sh 'echo Packaging...'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deploying...'
            }
        }

    }
}