pipeline {
    agent any 

// bloc qui contient ttes les etapes
    stage {
        stage('Build') {
            steps {
                // pour afficher le message dans la consolejenkins
                echo "Début du build de la calculatrice web"
            }
        }
        stage("Text") {
            steps {
                script {
                     //verification si le fichier index.html existe
                    if(fileExists('index.html')){
                       // Si oui → affiche ce message et le test passe
                        echo "Text réusssi : index.html existe"
                    } else {
                        // Si non → génère une erreur et arrête la pipeline
                        error "Echec du text : index.html est manquand"
                    }
                }
            }
        }
    } 
}
