pipeline {
    agent any

    stages {
        stage('Build master') {
            when { branch 'master' }
            steps {
                echo 'Building..'            
                sh 'docker build .'
            }
        }
        stage('Build dev') {
            when { branch 'dev' }
            steps {
                echo 'Building..'            
                sh 'docker build -f Dockerfile.dev .'
            }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
