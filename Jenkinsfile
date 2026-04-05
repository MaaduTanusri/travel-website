pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git 'https://github.com/MaaduTanusri/travel-website.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t travel-website .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 3000:3000 travel-website'
            }
        }
    }
}