pipeline {
agent any
triggers {
pollSCM('*/5 * * * *') // Vérifier toutes les 5 minutes
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
sh 'npm config ls'



// Ajoutez les commandes de build ici

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