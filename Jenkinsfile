
pipeline {
    agent any
    
    environment {
        // Define the Node.js tool name set up in Jenkins
        NODEJS_TOOL = 'NodeJS'
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository
                git 'https://github.com/Psalmzee/ECOMMERCE-DASHBOARD-WITH-ANGULAR-4.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // Install Node.js and npm dependencies
                sh "npm config set registry https://registry.npmjs.org/"  // Set registry if needed
                tool name: NODEJS_TOOL, type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
                sh 'npm install'
            }
        }
        
        stage('Build and Create Artifact') {
            steps {
                // Build the Angular application
                sh 'npm run build'
            }
        }
        
        
        // stage('Deploy') {
        //     steps {
        //         // For this example, we'll simply copy the built files to a remote server using SCP
        //         // Replace `user`, `your-server`, and `/path/to/destination` with your actual server details.
        //         sh 'scp -r dist/* user@your-server:/path/to/destination'
        //     }
        // }
    }
}
