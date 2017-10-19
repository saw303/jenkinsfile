pipeline {


    triggers {
        pollSCM '*/1 * * * *'
    }

    stages {

        stage('Compile') {
            sh 'echo Compiling...'
        }

        stage('Test') {
            sh 'echo Testing...'
        }

        stage('Package') {
            sh 'echo Packaging...'
        }

        stage('Deploy') {
            sh 'echo Deploying...'
        }

    }
}