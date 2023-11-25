pipeline {
    agent any

    stages {
        stage('Run Docker') {
            steps {
                script{
                    sh "docker-compose up -d"
                }
            }
        }
    }
}
