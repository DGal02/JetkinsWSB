pipeline {
    agent {
        docker {
            image 'node:24.12.0-alpine3.23'
            args '-u root:root'
        }
    }

    stages {
        stage('Install Dependencies') {
            steps {
                echo 'Instalowanie pakietów...'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Uruchamianie testów...'
                sh 'npm test'
            }
        }

        stage('Run App') {
            steps {
                echo 'Uruchamianie aplikacji...'
                sh 'node index.js'
            }
        }
    }
}