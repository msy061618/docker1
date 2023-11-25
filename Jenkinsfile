pipeline {
    agent any

    stages {
        stage('Verify installation') {
            steps {                
                    sh '''
                    docker --version
                    docker info
                    docker-compose --version
                    curl --version
                    jq --version
                    '''                
            }
        }

        stage('starting container'){
            steps{
                sh 'docker compose up -d --no-color --wait'
                sh 'docker compose ps'
            }
        }

        stage('Testing the 80 port container'){
            steps{
                sh 'curl http//:192.168.1.17 | jq'
            }        
        }
    }

}
