pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/Git-Mahesh06/devops-prt-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t prt-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 80:80 prt-app'
            }
        }
    }
}
