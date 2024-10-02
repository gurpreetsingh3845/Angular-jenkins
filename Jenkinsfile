pipeline {
    agent any
    tools {
        nodejs 'NodeJS' // Name of the NodeJS installation in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/highwire/sigma-oidc-fed.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'ng build'
            }
        }
        stage('Test') {
            steps {
                sh 'ng test --watch=false'
            }
        }
    }
}
