pipeline {
    agent any

    environment {
        PATH = "/usr/local/bin/npm"
    }

    triggers {
        pollSCM('*/5 * * * *')
    }

    stages {
        stage('Checkout') {
            steps {
                echo "Récupération du code source"
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo "Build du projet"
                echo "test sami"
                sh "npm install"
            }
        }
        stage('Deploy') {
            steps {
                echo "Déploiement du projet"
                sh "node app.js"
            }
        }
    }
}
