pipeline {
    agent {
        docker{
            image 'postman/newman:latest'
            args '-u root --entrypoint='
        }
    }
    stages {
         stage('Check version nodejs') {
            steps {
                sh 'newman --version'
            }
        }
        stage('Lancer le test') {
            steps {
                sh'newman run collections/collection.json -e env/preprod.json'
            }
        }
       
         
    }
} 
