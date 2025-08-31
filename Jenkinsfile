pipeline {
    agent any
    stages {

        stage('Création image Docker') {
            steps {
                sh 'docker build -t mezghich_amsdata_2025 .'
            }
        }
         stage('Lancement de la Stack Docker-Compose') {
                    steps {
                        sh 'docker compose -f Docker-compose.yml down'
                        sh 'docker compose -f Docker-compose.yml up -d'
                    }
         }
    }
}

