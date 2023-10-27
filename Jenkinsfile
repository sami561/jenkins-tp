pipeline {
agent any
tools {nodejs "default"}
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
sh "node app.js"

}
}
stage('Deploy') {
steps {
echo "Déploiement du projet"

}
}
}
}