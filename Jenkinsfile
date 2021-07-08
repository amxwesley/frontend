pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                when {
                    branch 'master'
                    sh 'docker build .'
                }
                when {
                    branch 'dev'
                    sh 'docker build -f Dockerfile.dev  .'
                    echo 'Dev branch builded.'
                }
            }
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
