pipeline {
    agent any

    tools {
        nodejs 'node-25'
    }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Run App') {
            steps {
                sh 'node index.js'
            }
        }
    }
}