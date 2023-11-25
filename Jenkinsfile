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
    post {
        always {
            // Clean up after the build
            script {
                sh 'docker-compose down'
            }
        }
    }
}
