pipeline {
    agent any

   tools {nodejs "nodejs"}

    triggers {
        pollSCM('*/5 * * * *')
    }

    stages {
        stage('Check Node.js') {
    steps {
     sh '/full/path/to/node -v'
    }
}
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
