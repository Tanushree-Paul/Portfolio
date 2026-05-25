pipeline {
    agent any

    environment {
        PATH = "/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin"
    }

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t portfolio .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8081:80 portfolio'
            }
        }
    }
}