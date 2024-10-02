pipeline {
    agent any

    environment {
        NODE_VERSION = 'v22.9.0'
    }

    tools {
        nodejs "${NODE_VERSION}"
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/highwire/sigma-oidc-fed.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                script {
                    // Install dependencies using npm
                    sh 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Build the Angular project
                    sh 'npm run build --prod'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run tests
                    sh 'npm test'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy the application
                    // This is a placeholder, replace with your actual deployment commands
                    sh 'echo "Deploying application..."'
                }
            }
        }
    }    
}
