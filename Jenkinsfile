pipeline {
    agent any 

    stages {                         // bloc qui contient ttes les etapes

        stage('Build') {
            steps {
                // pour afficher le message dans la consolejenkins
                echo "Début du build de la calculatrice web"
            }
        }

        stage('Test') {
            steps {
                script {
                     //verification si le fichier index.html existe
                    if(fileExists('index.html')){
                       // Si oui → affiche ce message et le test passe
                        echo "Test réussi : index.html existe"
                    } else {
                        // Si non → génère une erreur et arrête la pipeline
                        error "Échec du test : index.html est manquant"
                    }
                }
            }
        }
    } 
}
