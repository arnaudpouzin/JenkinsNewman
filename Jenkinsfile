pipeline {
    agent any 
    tools {nodejs "nodejs"}
    
    stages {

        stage ("Newman install") {
            steps {
            sh 'npm install -q newman'
            }
        }
        stage ("Run Newman") {
            steps {
                sh 'newman run Newman.postman_collection.json -e PROD_Newman.postman_environment.json'
            }
        }
    }

}