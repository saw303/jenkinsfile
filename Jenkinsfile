pipeline {

    agent any

    triggers {
        pollSCM '*/1 * * * *'
    }

    stages {

        stage('Initialize') {
            steps {
                sh './gradlew clean'
            }
        }

        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }

        stage('Package') {
            steps {
                sh './gradlew build'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deploying...'
            }
        }

        stage('Online tests') {
            parallel {
                stage('Selenium') {
                    steps {
                        sh "echo Hello"
                        sleep time: 7, unit: 'SECONDS'
                    }
                }
                stage('Stress Tests') {
                    steps {
                        sh "echo Hello"
                        sleep time: 3, unit: 'SECONDS'
                    }
                }
                stage('Extremely slow test') {
                    steps {
                        sh "echo Hello"
                        sleep time: 10, unit: 'SECONDS'
                    }
                }
            }
        }

    }
}