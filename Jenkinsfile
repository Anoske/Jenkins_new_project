pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Anoske/Jenkins_new_project/tree/main'
            }
        }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }

    post {
        success { echo 'Тесты прошли!' }
        failure { echo 'Тесты упали — деплой остановлен.' }
    }
}
