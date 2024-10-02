
pipeline {
    agent any

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
                    node {
                        bash 'npm install'
                    }
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Build the Angular project
                    node {
                        bash 'npm run build --prod'
                    }
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run tests
                    node {
                        bash 'npm test'
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy the application
                    // This is a placeholder, replace with your actual deployment commands
                    node {
                        bash 'echo "Deploying application..."'
                    }
                }
            }
        }
    }

    post {
        always {
            // Clean up workspace after build
            cleanWs()
        }
    }
}

