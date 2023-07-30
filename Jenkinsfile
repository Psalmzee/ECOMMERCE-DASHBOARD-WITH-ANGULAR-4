pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository
                git 'https://github.com/Psalmzee/ECOMMERCE-DASHBOARD-WITH-ANGULAR-4.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // Install Node.js
                tools {
                    nodejs 'NodeJS'
                }
                // Install npm dependencies
                sh 'npm install'
            }
        }
        
        stage('Build') {
            steps {
                // Build the Angular application
                sh 'npm run build'
            }
        }
        
    }
}
