pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout your code from version control system (e.g., Git)
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'dkgithub2516', url: 'https://github.com/dkgithub2516/Jenkins-proj.git']])
            }
        }
        stage('Install dependencies') {
            steps {
                // Install dependencies using pip
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run tests') {
            steps {
                // Run the tests using unittest
                sh 'python -m unittest discover'
            }
        }
    }
}
