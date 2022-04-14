pipeline {
    agent {label 'ec2-slave'}

    stages {
        stage('cloning repo') {
            steps {
                git branch: 'main', credentialsId: 'github-token', url: 'https://github.com/MostafaMAbdellateif/docker-counter-app.git'
            }
        }
        stage('run docker') {
            steps {
                sh "docker-compose up"
            }
        }
    }
}
