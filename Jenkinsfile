pipeline {
    agent any

    stages {
        stage('NPM Install') {
            steps {
                bat 'npm i'
            }
        }
        stage('NPM Audit') {
            steps {
                bat 'npm audit'
            }
        }
        stage('Run Integration tests') {
            steps {
                bat 'npm run test'
            }
        }
        stage('Deploy to Production') {
            steps {
                script {
                    input("Deploy to Production?")
                }
                echo 'Deploying...'
            }
        }
    }
}