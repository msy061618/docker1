pipeline {
    agent any

    stages {
        stage('Run Docker') {
            steps {
                script{
                    docker-compose up -d
                }
            }
        }
    }
}
